# Karlsen Transaction Report

Generates a CSV file for all your Karlsen transactions.

Currently in alpha - no expected SLA.

## Requirements

* NodeJS (v16+)

## Hosted

You can use the deployed version at https://report.karlsencoin.com/ or
you can host it yourself, to do so please do the following:

```
git clone https://github.com/karlsen-network/node-karlsen-transaction-report
cd node-karlsen-transaction-report
npm install
npm install serve
npm run build
npx serve --listen=3000
```

It is highly recommended to run the report utility behind a reverse
proxy like NGINX.

## Local

You can run this tool locally, to use it please do the following:

```
git clone https://github.com/karlsen-network/node-karlsen-transaction-report
cd node-karlsen-transaction-report
npm install
npm install esm
```

You need to create a file `addresses.txt` and add all your addresses,
one per line. For example:

```
karlsen:qqe3p64wpjf5y27kxppxrgks298ge6lhu6ws7ndx4tswzj7c84qkjlrspcuxw
karlsen:qzrq7v5jhsc5znvtfdg6vxg7dz5x8dqe4wrh90jkdnwehp6vr8uj7csdss2l7
```

To generate your transaction report run:

```
npm run generate
```

This will generate the file `karlsen-transactions.csv`. This CSV is
currently compatible with Koinly only.

## Notes

* Compound transactions and transactions sending to yourself are
  ignored.
* Assumes addresses from exchanges are treated as not your own.
* If you notice the report is inaccurate, first make sure you actually
  listed all addresses you care about in `addresses.txt`.

## Donation

Consider donating to [karlsen:qqe3p64wpjf5y27kxppxrgks298ge6lhu6ws7ndx4tswzj7c84qkjlrspcuxw](https://explorer.karlsennetwork.com/addresses/karlsen:qqe3p64wpjf5y27kxppxrgks298ge6lhu6ws7ndx4tswzj7c84qkjlrspcuxw)
