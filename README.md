# task3https://github.com/MohamedTa7a/task3/issues
#include <iostream>
#include <fstream>
#include <string>
using namespace std;
int main()
{
    ifstream infile;
    infile.open("task.txt");
    if(infile.fail())
    {
        cout<<"error oppening the file"<<endl;
    }
    else
    {
        string name="";
        string item;
        string serached ="dous";
        while(!infile.eof())
        {
            infile>>item;
            for (int i= item.size()-4 ; i < item.size() ; i++)
            {
                name+=item[i];
            }
            if(name==serached)
                cout<<item<<endl;
            name="";
        }
}
infile.close();
}







