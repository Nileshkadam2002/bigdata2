# bigdata2
java program interacts withs hdfs 
Assignment No. 2
Implement a Java program to interact with HDFS (reading and writing files).
import java.io.File;
public  class filehand  {
  public static void main(String []args) throws IOException
  {
      File obj1=new File(“/home/cloudera/Desktop/Firstfile.txt”);
      if (obj1.createNewFile())
          System.out.print(“File is Created”);
      else
          System.out.print(“File is Already exist”);
      FileWrite w1=new FileWriter(“/home/cloudera/Desktop/Firstfile.txt”);
      w1.write(“Welcome my first file is write”);
      w1.close();
      Scanner r1=new Scanner(obj1);
      while(r1.hasNextLine())
      {
             String data=r1.nextLine();
             System.out.println(data);
      }
   }
}
