# 🌊 Plasmr
### An extension of Solidity

Solidity is a beautiful language. From a transactional perspective, it is very well written. But with Plasmar, I want to address a few potential improvements. This is a personal think-out-loud repo, contributions welcome, of course.

```solidity
plasmr::stable;

contract samplePlasmr
{
  @message("Returns a number from parameter", uint _number);
  function returnExample(uint _number) public view returns (uint)
  {
    @message("This works!", {identifier:thisWorks});
    return _number;
  }
}
```

1. `plasmr::stable` in favor of `pragma` - this is to avoid floating solidity versions and such. You can define individual Plasmr versions as well.
2. Dropping the SPDX identifier line - Contracts should focus on core logic, with `plasmar.config` focusing on licenses and such. This will be similar to `cargo.toml` where dependencies and such are declared.
3. `@message` is a decorator-esque syntax that allows users to emit messages for every function. `@message` at any part can allow users to emit functions. 

A few more potential improvements - 
1. Drop `selfdestruct` opcode.
2. Implement easier inline assembly.
3. Work on introducing easier library development and non-npm package management.

