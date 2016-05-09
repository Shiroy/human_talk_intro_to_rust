##  Traits

```rust
trait HasArea { fn area(&self) -> f64; }

struct Circle { x:f64, y:f64, radius:f64 }
impl HasArea for Circle {
    fn area(&self) -> f64 { PI*self.radius*self.radius }
}

struct Rect { x1:f64, y1:f64, x2:f64, y2:f64 }
impl HasArea for Rect {
    fn area(&self) -> f64 { (self.x2-self.x1).abs()*(self.y2-self.y1).abs() }
}

fn  main()  {
    let r = Rect { x1:3.0, y1:3.0, x2:10.0, y2: 7.0};
    let c = Circle { x:3.0, y:3.0, radius:2.0 };
    println!("{:?} {:?}", r.area(), c.area());
}
```

```text
28 12.566371
```

note:
    Equivalent classes abstraites pures.
    Permet le polymorphisme et le dispatching dynamique
