issue was in the rv32i.yaml

the test was designed to run on rv32i machine but in the config file there was an issue we ware also generating test case fo   rel_rv64m: 10

which was causing make file to fail
