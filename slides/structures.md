##  Structures

```rust
use std::num::Float;

struct Point {
    x:f64, y:f64
}

fn  main()  {
    let a = Point { x:3.0, y:4.0 };
    let dist = (a.x*a.x + a.y*a.y).sqrt();
    println!("{} {} {}", a.x, a.y, dist);
}
```

```text
3 4 5
```

note:
    Equivalent aux classes.
    Pas de classes abstraites.
