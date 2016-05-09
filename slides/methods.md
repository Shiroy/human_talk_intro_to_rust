##  Structures and methods

```rust
use std::f64::consts::PI;
use std::num::Float;

struct Circle { x:f64, y:f64, radius:f64 }
impl Circle {
    fn area(&self) -> f64 { PI*self.radius*self.radius }
}

fn  main()  {
    let c = Circle { x:3.0, y:3.0, radius:2.0 };
    println!("{:?}", c.area());
}
```

```text
12.566371
```

note:
    Implémentation dans des blocs modulaires.
    Méthodes statiques.
