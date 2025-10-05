# Programs-


ChatGPT
You said:
Practice the following 
Command line argument
Inline function 
Default argument 
Static member function 
Friend function 
Function overloading 
Object as argument 
Constructor & Desructor 
Operator overloading 
All types of inheritance 
Virtual base class abstract class

There are my practical exam topics
ChatGPT said:
Perfect 👍 These are all important C++ practical exam topics.
Let’s quickly go over what you should practice for each topic — including sample programs and what examiners usually ask.

🧩 1. Command Line Argument
Concept: Passing arguments to main() from the terminal.

#include <iostream>
using namespace std;
int main(int argc, char* argv[]) {
    cout << "Number of arguments: " << argc << endl;
    for(int i = 0; i < argc; i++)
        cout << "Arg " << i << ": " << argv[i] << endl;
    return 0;
}
⚡ 2. Inline Function
Concept: Function defined inside a class or with inline keyword to reduce function call overhead.

#include <iostream>
using namespace std;
inline int square(int x) { return x * x; }
int main() {
    cout << "Square of 5: " << square(5);
}
⚙️ 3. Default Argument
Concept: Giving default values to function parameters.

#include <iostream>
using namespace std;
int add(int a, int b=10) { return a + b; }
int main() {
    cout << add(5) << endl;    // Uses default 10
    cout << add(5,15);
}
🔒 4. Static Member Function
Concept: Shared among all objects; can access only static data.

#include <iostream>
using namespace std;
class Demo {
    static int count;
public:
    static void show() { cout << "Count = " << count; }
};
int Demo::count = 10;
int main() { Demo::show(); }
🧑‍🤝‍🧑 5. Friend Function
Concept: Function that can access private data of a class.

#include <iostream>
using namespace std;
class Box {
    int width;
public:
    Box(int w) { width = w; }
    friend void show(Box b);
};
void show(Box b) {
    cout << "Width = " << b.width;
}
int main() { Box b(10); show(b); }
🔁 6. Function Overloading
Concept: Same function name, different parameters.

#include <iostream>
using namespace std;
int add(int a,int b){return a+b;}
float add(float a,float b){return a+b;}
int main(){
    cout<<add(3,4)<<endl;
    cout<<add(2.5f,3.5f);
}
📦 7. Object as Argument
Concept: Passing an object to a function.

#include <iostream>
using namespace std;
class Test {
    int a;
public:
    void set(int x){a=x;}
    void show(Test t){cout<<"Value = "<<t.a;}
};
int main(){
    Test t1,t2;
    t1.set(10);
    t2.show(t1);
}
🧱 8. Constructor & Destructor
Concept: Initialize and clean up objects.

#include <iostream>
using namespace std;
class Demo {
public:
    Demo() { cout<<"Constructor called\n"; }
    ~Demo() { cout<<"Destructor called\n"; }
};
int main(){
    Demo d;
}
➕ 9. Operator Overloading
Concept: Redefine operators for user-defined types.

#include <iostream>
using namespace std;
class Complex {
    int r, i;
public:
    Complex(int x=0,int y=0){r=x;i=y;}
    Complex operator+(Complex c){
        return Complex(r+c.r, i+c.i);
    }
    void show(){cout<<r<<"+"<<i<<"i";}
};
int main(){
    Complex c1(2,3), c2(4,5), c3;
    c3 = c1 + c2;
    c3.show();
}
🧬 10. Inheritance Types
(a) Single Inheritance
class A { public: void showA(){cout<<"A";} };
class B: public A { public: void showB(){cout<<"B";} };
(b) Multiple Inheritance
class A { public: void showA(){cout<<"A";} };
class B { public: void showB(){cout<<"B";} };
class C: public A, public B { };
(c) Multilevel Inheritance
class A { public: void showA(){cout<<"A";} };
class B: public A { public: void showB(){cout<<"B";} };
class C: public B { public: void showC(){cout<<"C";} };
(d) Hierarchical Inheritance
class A { public: void showA(){cout<<"A";} };
class B: public A{};
class C: public A{};
(e) Hybrid Inheritance
(Mix of multiple + multilevel, often uses virtual base class)

🧱 11. Virtual Base Class
Used to solve diamond problem in multiple inheritance.

#include <iostream>
using namespace std;
class A { public: void show(){cout<<"Class A\n";} };
class B: virtual public A{};
class C: virtual public A{};
class D: public B, public C{};
int main(){ D obj; obj.show(); }
🧩 12. Abstract Class
Contains at least one pure virtual function.

#include <iostream>
using namespace std;
class Shape {
public:
    virtual void area() = 0;  // Pure virtual
};
class Circle : public Shape {
public:
    void area(){ cout<<"Area = 3.14*r*r"; }
};
int main(){
    Circle c;
    c.area();
}
