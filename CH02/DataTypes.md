# Data Types

Rust programming language သည် Static Typed Programming Language ဖြစ်သည့်အတွက် code ရေးသားချိန်တွင် variable များ၏ type ကို programmer နှင့် compiler မှ သိဖို့လိုအပ်ပါတယ်။

Python, JavaScript ကဲ့သို့သော Dynamic Typed Programming Language များကိုလေ့လာဖူးသူများအနေနှင့် ဤအချက်သည် အစပိုင်းတွင် အနည်းငယ် စိတ်ရှုပ်စရာဖြစ်နိုင်ပေမဲ့ သတိမထားမိသော type error များကို compile time တွင်စစ်ထုတ်နိုင်သည့်အတွက် error ရှင်းရနည်းရန်နှင့် program performance အတွက်များစွာအထောက်အကူဖြစ်တာကိုတွေ့ရမှာပါ။

ဒီအပိုင်းမှာဆိုရင် scalar types ဖြစ်တဲ့

* Integer Types
* Floating Point Types
* Character Type
* Boolean Type

compound types တွေဖြစ်တဲ့

* array
* tuple

တို့အကြောင်းကိုရှင်းပြပေးမှာဖြစ်ပါတယ်။

တခြား programming language တွေမှာ တွေ့နေကျဖြစ်တဲ့ String type ကတော့ rust မှာ collection type ဖြစ်တဲ့အတွက် အဆုံးကျမှ အကျဥ်းချုပ်ရှင်းပြပေးပါမယ်။

</br>

## Integer Types

Programming Language တွေထဲမှာမှ System Programming တွေက programmer တွေကို memory တွေကို ကိုယ်တိုင် manage ရတဲ့ အတွက် အနည်းငယ်ခက်တယ်လို့ထင်ရပေမဲ့ Computer Science ကိုလေ့လာဖို့နဲ့ performance ကောင်းတဲ့ program ရေးဖို့အတွက်အရမ်းအဆင်ပြေပါတယ်။ 

Rust Language ကလည်း system programming language ဖြစ်တဲ့ အတွက် programmer တွေကို ကိုယ်တိုင် memory manage ခွင့်ပေးထားပါတယ်။ ဒါကြောင့်ပဲ Rust မှာ unsign or sign 8 bits, 16 bits, 32 bits, 64 bits, 128 bits စတဲ့ integer types များစွာရှိပါတယ်။ နောက်ပြီး machine ရဲ့ architecture ကိုလိုက်ပြီး range ပြောင်းလဲနိုင်တဲ့ `usize` `isize` စတဲ့ integer types များလည်းရှိပါတယ်။ 

Integer types တွေအပြည့်အစုံကိုမဖော်ပြခင် Python/Js စတဲ့ Dynamic Language background ကနေလာတဲ့ programmer တွေအနေနဲ့ ဘာကြောင့် integer types တွေအရမ်းများနေရလဲဆိုပြီး စိတ်ရှုပ်လောက်မယ်ထင်ပါတယ်။ memory တွေမှာ အနည်းဆုံး unit အဖြစ် 8bits နေရာယူပါတယ်။ RGB ရဲ့ range ကို program ထဲ ထည့်ရေးမယ်ဆိုပါစို့ color တစ်ခုစီရဲ့ range က 0 ကနေ 255 အထိပဲရှိပါတယ်။ unsign 8 bits integer ရဲ့ range က 0 - 255 အထိရှိတဲ့ အတွက် Color encode ဖို့အတွက်သင့်တော်ပါတယ်။ ဒါဆို unsign 8bits intသုံးမယ်ဆိုရင် RGB သုံးခုလုံးအတွက်မှ 24bit ပဲကုန်ကျမှာပါ။ Python တို့လို programming language တွေမှာ int types နဲ့ encode မယ်ဆိုရင် Color တစ်ခုစီအတွက် 32bits သို့ 64bits ကုန်မှာပါ။ System Programming Language တွေရဲ့ advantage အနေနဲ့ Resource ကိုခြွေတာလို့ရပါမယ်။ Programming နယ်ပယ်ထဲမှာ ဘယ်ဟာမှအလကားမရပါဘူး။ Trade off အနေနဲ့ programmer က type ကို ဂရုစိုက်ရတဲ့ အတွက် နည်းနည်းပိုအလုပ်ရှုပ်ပါတယ်။ ဒါဆို ဘာကြောင့် integer types များလဲဆိုတာရှင်းလောက်ပြီထင်ပါတယ်။

ဒါဆို integer types တွေကိုအကျိုးရှိရှိအသုံးချဖို့အတွက် type တစ်ခုချင်းစီရဲ့ range ကို သိဖို့လိုပါတယ်။ unsign integer တွေရဲ့ range ကိုတွက်ထုတ်ဖို့အတွက်  `(2 ^ n) - 1` ဆိုတဲ့ ပုံသေနည်းကိုသုံးရပါတယ်။ ဒါဆို 8bits unsign integer ရဲ့ အကြီးဆုံးဖြစ်နိုင်တဲ့တန်ဖိုးကိုတွက်ကြည့်ရအောင် `(2 ^ 8) - 1 = 255` ရပါလိမ့်မယ်။ ကျန်တဲ့ unsign integer တွေရဲ့ ဖြစ်နိုင်တဲ့ အကြီးဆုံးတန်ဖိုးတွေကို ဒီပုံသေနည်းသုံးပြီးရှာနိုင်ပါတယ်။

