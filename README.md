# To run the code we will have to install Go progmamming language

# After installing Go, run the following commands in the code root directory:
# This command will install the packages that are required to run the go project
1) go install -v

# This command is used to start the boltDB servers and replicas
# Passing the http addr, config files and shard names as argument variables
2)go run main.go -db-location=Farhan.db -http-addr=127.0.0.2:8080 -config-file=sharding.toml -shard=Farhan &
go run main.go -db-location=Farhan-r.db -http-addr=127.0.0.22:8080 -config-file=sharding.toml -shard=Farhan -replica &

go run main.go -db-location=Mayur.db -http-addr=127.0.0.3:8080 -config-file=sharding.toml -shard=Mayur &
go run main.go -db-location=Mayur-r.db -http-addr=127.0.0.33:8080 -config-file=sharding.toml -shard=Mayur -replica &

go run main.go -db-location=Fahad.db -http-addr=127.0.0.4:8080 -config-file=sharding.toml -shard=Fahad &
go run main.go -db-location=Fahad-r.db -http-addr=127.0.0.44:8080 -config-file=sharding.toml -shard=Fahad -replica &

go run main.go -db-location=Lebron.db -http-addr=127.0.0.5:8080 -config-file=sharding.toml -shard=Lebron &
go run main.go -db-location=Lebron-r.db -http-addr=127.0.0.55:8080 -config-file=sharding.toml -shard=Lebron -replica


