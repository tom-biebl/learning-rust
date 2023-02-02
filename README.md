tombiebl
# learning-rust
all coding exercises of the book "The Rust Programming Language"


## my rust cheatsheet
### chapter 2 some simple stuff
In chapter two we built a simple guessing game. The concept is very simple, the programm generates a random unsigned integer (u32) and asks the user to guess the generated number.

#### conclusion:
##### read input of user
- To read the input of an user in "Rust" we import the library io which comes with the standard library (std)
- A simple example would be:

use std::io;

fn main() {
let mut inp = String::new;
io::stdin().read_line(&mut inp)
  .expect("Failed to read line");
  
 println!("You wrote: {}", inp);
}

note: the "read_line" function reads the user input, as parameters we pass a reference to the input variable. We need to use "&mut" to mutate da value of "inp".

##### parse the string value of "inp" into an unsigned integer (u32)
- To parse the one datatype into another, we need to use the following code:

let inp: u32 = guess.trim().parse()
    .expect("handling some stuff");
    
