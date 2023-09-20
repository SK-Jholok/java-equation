# java-euqation
Finding the values of a equation 
<br>
 public static void main(String[] args) {
     Scanner sc=new Scanner(System.in);
        System.out.println("Input the value of a,b,c=");
       double a=sc.nextDouble();
        double b=sc.nextDouble();
        double c=sc.nextDouble();
       double root1, root2;
       //calculate determination
       double determinant= b*b-4*a*c;
       //check determination is grater than 0
        if(determinant>0){

            root1=(-b + Math.sqrt(determinant))/(2*a);
            root2=(-b-Math.sqrt(determinant))/(2*a);
            System.out.format("root1 = %.2f and root2 = %.2f", root1, root2);
        }
        else if (determinant ==0) {
            root1=root2=-b/2*a;
            System.out.format("root1=root2=%2.f", root1, root2);
        }
        else {
             double real=-b/2*a;
             double imaginary= Math.sqrt(-determinant)/2*a;
            System.out.format("root1=%.2f+%.2fi", real, imaginary);
            System.out.format("\nroot2= %.2f-%2fi", real, imaginary);
        }
