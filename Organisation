import java.io.*;
public class Organisation extends Thread
 {
    public static void main(String[] args) {
        String str = null;
        String str1 = null;

        try {
            BufferedReader br = new BufferedReader(new FileReader("StudentDetails.txt"));
            String line;
            while ((line = br.readLine()) != null) 
            {
               System.out.println(line);
            }
            BufferedReader br1 = new BufferedReader(new FileReader("Employee.txt"));
            String linel;
            while ((linel = br1.readLine()) != null) {
                System.out.println(line);
            }
        } catch (Exception e) 
        {
            System.out.println(e);
        }

        String a = str;
        String b = str1;

        Thread t1 = new Thread() {
            public void run() {
                synchronized (a) {
                    System.out.println("Thread t1 is locked with a");
                    synchronized (b) {
                        System.out.println("Thread t1 is locked with b");
                    }
                }
            }
        };

        Thread t2 = new Thread() {
            public void run() {
                synchronized (b) {
                    System.out.println("Thread t2 is locked with b");
                    synchronized (a) {
                        System.out.println("Thread t2 is locked with a");
                    }
                }
            }
        };

        t1.start();
        t2.start();
    }
}
