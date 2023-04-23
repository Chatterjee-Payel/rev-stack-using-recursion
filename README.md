# rev-stack-using-recursion
class Solution{
public:
 void InsertAtBottom(stack<int> &St,int element){
     if(St.empty())
     {
        St.push(element);
        return;    
    }
    int num=St.top();
    St.pop();
   InsertAtBottom(St,element);
    St.push(num);
    return;
 }
    void Reverse(stack<int> &St){
        if(St.empty())
        {
            return;
        }
       int num=St.top();
       St.pop();
       Reverse(St);
       InsertAtBottom(St,num);
       return;
    }
};
