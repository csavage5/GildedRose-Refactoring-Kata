# TODO
- create tests to verify existing functionality
- move string comparisons to enums

# Item types + attribute rules

### General rules
- `Quality` and `SellIn` -=1 each day
- When `SellIn` reaches `0`, `Quality` -=2 each day
- Ceiling of `Quality` is `50`

### Item-specific rules
- `Aged_Brie`
    - `Quality` *increases* every day
- `Sulfuras`
    - `Quality` == 80, never changes
    - `SellIn` is disregarded
- `Backstage_Passes`
    - `Quality` *increases* by +=2 when `SellIn` <= 10, +=3 when `SellIn` <= 5 
    - `Quality` == `0` after `SellIn` == 0
- `Conjured`
    - `Quality` -= 2 each day

# Test scenarios
