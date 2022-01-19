//# PolyMorphism
//polymorphism in C++ OOP

#include<iostream>
using namespace std;
class Shape{
	public:
		virtual void area()=0;
	};
	class Triangle: public Shape{
		public:
			void area(){
				cout<<"area of triangle:"<<endl;
			}
	};
	class Rectangle :public Shape{
		public:
			void area(){
				cout<<"The area of rectangle "<<endl;
			}
	};
		int main(){
			Shape *ptr;
			Triangle t;
			Rectangle r;
			ptr=&t;
			ptr->area();
	
			ptr=&r;
			ptr->area();
			return 0;
		}
