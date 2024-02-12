# schemacrawler

generate schema file from database:
```bash
docker run --rm -it -v ${PWD}:/home/schcrwlr \
  schemacrawler/schemacrawler:v16.21.1 \
  /opt/schemacrawler/bin/schemacrawler.sh \
  --server=postgresql \
  --host=172.31.23.100 \
  --port=30267 \
  --database=magma \
  --user=postgres \
  --password=postgres \
  --schemas=public \
  --info-level=standard \
  --command=schema \
  --output-format=png \
  --output-file=graph.png
```
> format can be `png` or `svg` and default port is `5432`

Install psql client
```bash
sudo apt install postgresql-client -y
```

connect to database:
```bash
export PGPASSWORD=postgres
psql -U postgres -d magma -h 172.31.23.100 -p 30267
```
