# Priority-Queue
The Java code for a simple array-based priority queue
 public static void main(String[] args) {
      int a=10;
      pr q=new pr(a);
      System.out.println(q.IsEmpty());
       q.insert(4);
       q.insert(2);
       q.insert(8);
       q.insert(5);
       q.insert(1);
       System.out.println(q.peek());
       q.insert(9);
       q.insert(10);
       q.insert(3);
       q.insert(6);
       q.insert(7);
       q.insert(11);
       System.out.println(q.IsFull());
       a=q.d();
       for(int i=0;i<a;i++){
            System.out.println(q.del());
       }
        System.out.println(q.IsFull());
         System.out.println(q.IsEmpty());
       
       
       
    }
    public class pr {
    
    private int max;
    private int n;
    private int[] q;
     public pr(int s){
     max=s;
     q=new int[max];
     n=0;
     }
     
     public void insert(int k){
         int j;
     if(n==max)
       System.out.println("LOL");
     else if(n==0)
         q[n++]=k;
     else{
         for(j=n-1;j>=0;j--){
             if(k>q[j])
                 q[j+1]=q[j];
             else
                 break;
         }
         q[j+1]=k;
         n++;
       
     } }
     
     public int del(){
     return q[--n];}
     
     public boolean IsEmpty(){
     return n==0;}
     
     public boolean IsFull(){
     return n==max;}
public int peek(){
return q[n-1];}   
public int d(){
return n;}
}
