---
title: "Lesson 01 - File I/O"
---

## References

- [Tutorialspoint Files and I/O](http://www.tutorialspoint.com/java/java_files_io.htm)
- [Java Doc - Basic I/O](http://docs.oracle.com/javase/tutorial/essential/io/index.html)

## Input from Console / Files

- You can use an InputStreamReader to read from standard (console) input.

    ```java
    InputStreamReader isr = new InputStreamReader(System.in);
    ```

- You can use a FileReader to read from file input

    ```java
    FileReader fr = new FileReader("input.txt");
    ```

#### Demo

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class FileReadDemo {

	public static void main(String[] args){

		try {
			BufferedReader fileIn;
			String line;

			// reading from standard input
			fileIn = new BufferedReader(new InputStreamReader(System.in));

			// reading from a file
			//fileIn = new BufferedReader(new FileReader("filename.txt"));

			while((line = fileIn.readLine()) != null){

				// remove any leading or trailing whitespace
				//	also removes newline (\n) or carriage return (\r)
				line = line.trim();
				System.out.println( line );
			}
			fileIn.close();

		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
```
## File Output

#### Demo

```java
import java.io.BufferedWriter;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStreamWriter;
import java.io.Writer;

public class FileWriteDemo {

	public static void main(String[] args) {

		try{
			Writer writer;

			writer = new BufferedWriter(new OutputStreamWriter(
			          new FileOutputStream("filename.txt"), "utf-8"));

			for( int i=0; i<10; i++ ){

				// add a carriage return (\r) at the end of each line
				writer.write( "Hi " + i + "!\r");
			}

			writer.close();
		}
		catch(IOException e){
			e.printStackTrace();
		}
	}
}
```
