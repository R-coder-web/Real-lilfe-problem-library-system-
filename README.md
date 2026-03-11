# Real-lilfe-problem-library-system-
#include <iostream>
#include <string>
using namespace std;
class Book{
    public:
    string title;
    string Author;
    int id;
    float price;
    void takeinfo(){
    cout<<"enter the tittle name: "<<endl;
    cin>>title;
    cout<<"enter the Author name: "<<endl;
    cin>>Author;
    cout<<"enter the id: "<<endl;
    cin>>id;
    cout<<"enter the price: "<<endl;
    cin>>price;
    }
    double discount(){
    return price*.85;
    }
    void getinfo(){
    cout<<"Title: "<<title<<endl;
    cout<<"author: "<<Author<<endl;
    cout<<"Id: "<<id<<endl;
    cout<<"discount price: "<<discount()<<endl;
    }
};
int main(){
    int n;
    cout<<"enter the amount of taking information: "<<endl;
    cin>>n;
Book b1[n];
for(int i=0;i<n;i++){
    cout<<i+1<<endl;
    b1[i].takeinfo();
}
bool found =false;
for(int i=0;i<n;i++){
    if(b1[i].discount()>50){
        b1[i].getinfo();
        found=true;
    }
}
if(!found){
    cout<<"No books found in this range"<<endl;
}
return 0;

}

