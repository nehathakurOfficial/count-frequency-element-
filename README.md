#include<bits/stdc++.h>
using namespace std;

void  countfreq(int arr[],int n)
{
    vector<bool>visited(n , false);
    for(int i = 0; i< n; i++){


       
        if(visited[i] == true)
        continue;


        //count frequency
        int count = 1;
        for(int j = i + 1;j< n; j++ ){
            if(arr[i] == arr[j]){
                visited[j] = true;
                count ++;
            }
        }
        cout<<"count of "<<arr[i] <<  "=  " <<count <<endl;
    }
}

int main(){
    int arr[] = { 10,5,10,15,10,5};
    int n = sizeof(arr)/sizeof(arr[0]);
    countfreq(arr,n);

    return 0;

}
