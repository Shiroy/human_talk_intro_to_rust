##  Pattern matching

```rust
enum Resultat {
    Erreur(String),
    Ok(i32)
}

fn diviser(a: i32, b: i32) -> Resultat {
    if b == 0 {
        Erreur(String::from("Division par 0"))
    }
    else {
        Ok(a/b)
    }
}

fn main() {
    match diviser(4, 2) {
        Erreur(msg) => println!("{}", msg),
        Ok(result) => println!("Resultat : {}", result),
    }
}
```

```text
Resultat : 2
```

note:
    Type pouvant prendre un ensemble de valeur + payload.
    Exemple Option / Result
