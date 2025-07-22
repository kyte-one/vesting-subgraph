
## Steps for running in Dev mode

1. Specify the contract address of the locally deployed Smart Contract, the emitted Events and their handlers in `subgraph.template.yaml` file.

2. `npm run codegen` whenever there are changes in `schema.graphql` file or the Contract abi(abis/*.json)

3. `npm run prepare:local` to create `subgraph.yaml` file.

4. Start a graph-node instance with `docker-compose up`

5. `npm run create-local` to create an instance of the graph (run only first time. Subsequent Deployments are done on the same graph node instance)

6. `npm run deploy-local` to deploy event handler mappings to the graph node.



## Deployment Steps


create a graph studio project

1. `npm install -g @graphprotocol/graph-cli`

2. `graph init graph init kte-vesting-bsc`

3. `graph auth xxxx`

4. `npm run prepare:bsc`

5. `graph codegen && graph build`

6. `graph deploy kte-vesting-bsc`