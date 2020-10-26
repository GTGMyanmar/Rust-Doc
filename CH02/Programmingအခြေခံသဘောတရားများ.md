# Programming အခြေခံသဘောတရားများ

ဒီတစ်ခါမှာတော့ တစ်ခြား programming language တွေမှာ တွေ့မြင်နေကျဖြစ်တဲ့ မဖြစ်မနေသိထားရမဲ့ variable declaration တွေ basic data types, function တွေကိုတည်ဆောက်ပုံတွေနဲ့ control flow တွေကိုဘယ်လိုလုပ်ရလဲစတာတွေကိုလေ့လာရမှာဖြစ်ပါတယ်။

> Variables တွေကိုဘယ်လို declare ရလဲ မပြောခင်မှာ _keyword_ တွေအကြာင်းကိုအရင်လေ့လာကြည့်ရအောင်။ Keywords တွေဆိုတာက programming language တစ်ခုစီမှာ နဂိုကတည်းက လုပ်ဆောင်ချက်တွေကိုသတ်မှတ်ထားပြီးသားဖြစ်တဲ့ စာလုံးတွေဖြစ်ပါတယ်။ ၄င်း keywords တွေကို ကျွန်တော်တို့ variables တို့ function name တို့အဖြစ် declare လို့ရမှာမဟုတ်ပါဘူး။

</br>

## Variables Declaration

Variable တွေကို ဘယ်လိုကြေညာရလဲမပြောခင်မှာ variable တွေဆိုတာဘာလဲ ဘယ်လိုအလုပ်လုပ်လဲဆိုတာအရင်ကြည့်ရအောင်။

variable သဘောတရားဆိုတာကျွန်တော်တို့နဲ့ရင်းနှီးနေကျဖြစ်ပါတယ်။ မှတ်ပုံတင်တို့မှာ `နာမည်: ဘယ်သူဘယ်ဝါ, အဖအမည်: ဘယ်သူဘယ်ဝါ` ဆိုတာမျိုးတွေရမှာပါ စာရင်းစစ်တဲ့သူက နာမည်သိချင်ရင် အများကြီးမေးစရာမလိုပါဘူး သူက `နာမည်` လို့ပြောလိုက်တာနဲ့ ကိုယ့်နာမည်ကို မေးမှန်းသိကြပါတယ်။ ဒီသဘောတရားမှာ `နာမည်` ဆိုတာသည် `variable` ကိုကိုယ်စားပြုတာဖြစ်ပါတယ်။

ဒါဆို variable ဆိုတာဘာလဲသဘောပေါက်လောက်ပြီမို့အောက်က code မှာ variable ဘယ်လို declare လဲကြည့်ကြရအောင်။

```Rust
fn main() {
    let x = 5;
}
```

Rust မှာ variable ကို ကြေညာဖို့အတွက် `let` ဆိုတဲ့ keyword ကိုသုံးရပါတယ်။ `=` ကိုတော့ asignment operator လို့ခေါ်ပါတယ်။ အဲဒီ code ရဲ့ အဓိပ္ပါယ်ကတော့ `x တန်ဖိုး 5 ဖြစ်ပါစေ` လို့ဖော်ပြပါတယ်။ code ရဲ့အဆုံးက `;` လေးကိုထည့်ဖို့မမေ့နဲ့ဦးနော်။

အောက်က code လေးကိုထပ်ကြည့်လိုက်ရအောင်။

```Rust
fn main() {
    let x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

run လိုက်ရင် အောက်ကအတိုင်း error ထွက်လာမှာကိုမြင်ရမှာဖြစ်ပါတယ်။

```console
(base) aung@aung:~/col/rust/project/Code/variables$ cargo run
   Compiling variables v0.1.0 (/home/aung/col/rust/project/Code/variables)
error[E0384]: cannot assign twice to immutable variable `x`
 --> src/main.rs:4:5
  |
2 |     let x = 5;
  |         -
  |         |
  |         first assignment to `x`
  |         help: make this binding mutable: `mut x`
3 |     println!("The value of x is: {}", x);
4 |     x = 6;
  |     ^^^^^ cannot assign twice to immutable variable

error: aborting due to previous error

For more information about this error, try `rustc --explain E0384`.
error: could not compile `variables`.

To learn more, run the command again with --verbose.
```

ဘာကြောင့် error တက်လဲဆိုတာအဖြေရှာကြည့်ရအောင်။ console output ထဲမှာ `cannot assign twice to immutable variable` ဆိုတဲ့ စာကိုတွေ့ရမှာဖြစ်ပါတယ်။ Rust မှာ immutable နဲ့ mutable variable နှစ်မျိုးပါတယ်။ immutable variable ဆိုတာကတော့ variable ကို declare ပြီးရင် တန်ဖိုးပြန်ပြောင်းလို့မရပါဘူး။ တကယ်လို့တန်ဖိုးကိုပြန်ပြောင်းချင်ရင် mutable variable ဖြစ်ရပါမယ်။ Rust မှာဘာကြောင့် ဒီ rule ကိုသုံးလဲဆိုရင် multi-thread program တွေမှာ တန်ဖိုးတွေ ကိုယ်သတိမထားမိဘဲ မတော်တဆပြောင်းပြီး bug တွေဖြစ်လာခြင်းမှကာကွက်ဖိုဖြစ်ပါတယ်။ variable ကို mutable အဖြစ်ကြေညာဖို့ဆိုရင် `mut` keyword ကိုသုံးရမှာဖြစ်ပါတယ်။ အောက်က code ကိုကြည့်ကြည့်ပါ။

```Rust
fn main() {
    let mut x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```
