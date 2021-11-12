# schemacrawler

generate schema file from database:
```bash
docker run --rm -it -v ${PWD}:/home/schcrwlr \
  schemacrawler/schemacrawler \
  /opt/schemacrawler/schemacrawler.sh \
  --server=postgresql \
  --host=192.168.0.52 \
  --database=magma \
  --user=postgres \
  --password=postgres \
  --port=5432 \
  --schemas=public \
  --info-level=standard \
  --command=schema \
  --output-format=svg \
  --output-file=graph.svg
```
