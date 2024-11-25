<div align="center">
    <img alt="Tado's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=TadoTheMiner&show_icons=true&hide_border=true&theme=catppuccin_mocha">
</div>

```rust
use std::fmt;

fn main() {
    let tado = Rustacean{name: "Tatesa", pronouns: &Pronouns::TheyThem, capitalise_pronouns: true, distro: "NixOS"};
    println!("{tado}");
}

#[allow(dead_code)]
struct Rustacean<'a> {
    name: &'a str,
    pronouns: &'a Pronouns<'a>,
    capitalise_pronouns: bool,
    distro: &'a str,
}

#[allow(dead_code)]
enum Pronouns<'a> {
    HeHim,
    SheHer,
    TheyThem,
    ItIts,
    Other(&'a str),
}

impl fmt::Display for Rustacean<'_> {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "Hi! I am {}, and use {} BTW!", self.name, self.distro)
    }
}

```
