Add Parent-Child Chain Relationships
If a chain is an L2 or a shard of another chain, you can add a parent field to link it to its parent chain. This helps tools understand the relationship between chains.

Example Contribution:
Add a parent relationship for an L2 chain.
{
  ...
  "parent": {
    "type": "L2",
    "chain": "eip155-1",
    "bridges": [{"url": "https://bridge.mycustomchain.com"}]
  }
}

Deprecate Old Chains
If a chain is no longer active, you can mark it as deprecated by adding a status field. This ensures that the chain is not deleted (to avoid replay attacks) but is clearly marked as inactive.

Example Contribution:
Deprecate a testnet that is no longer in use.

{
  ...
  "status": "deprecated"
}
