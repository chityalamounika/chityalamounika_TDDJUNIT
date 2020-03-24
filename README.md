# chityalamounika_TDDJUNIT

#RemoveACharBeg 

package epamTask.tddJunitDemo;

public class RemoveACharBeg {

	public String remove(String string) {
		
		String result=string;
		if(string.length()>0)
		{
			if(string.charAt(0)=='A')
			{
				if(string.charAt(1)=='A')
				{
					result=string.substring(2,string.length());
				}
				else
				{
					result=string.substring(1,string.length());
				}
			}
			else if(string.charAt(1)=='A')
			{
				result=string.substring(0,1)+string.substring(2,string.length());
			}
		}
		return result;
	}

}




#RemoveAchar

package epamTask.tddJunitDemo;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class RemoveAChar {

	/*
	 * TODO list for my feature
	 * 1.case1:"ABCD" => "BCD"
	 * 2.case2:"AACD" => "CD"
	 * 3.case3:"BACD" => "BCD"
	 * 4.case4:"BBAA" => "BBAA"
	 * 5.case5:"AABAA" => "BAA"
	 * 6.case6:"" => ""
	 * 7.case7:"B" => "B"
	 */
	RemoveACharBeg removeAchar;
	
	@BeforeEach
	void function()
	{
		removeAchar=new RemoveACharBeg();
	}

	@Test
	void case1() {
		assertEquals("BCD",removeAchar.remove("ABCD"));
	}

	@Test
	void case2() {
		assertEquals("CD",removeAchar.remove("AACD"));
	}

	@Test
	void case3() {
		assertEquals("BCD",removeAchar.remove("BACD"));
	}
	
	@Test
	void case4() {
		assertEquals("BBAA",removeAchar.remove("BBAA"));
	}
	
	@Test
	void case5() {
		assertEquals("BAA",removeAchar.remove("AABAA"));
	}
	
	@Test
	void case6() {
		assertEquals("",removeAchar.remove(""));
	}

	
}






#pom.xml

<?xml version="1.0"?>

-<project xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://maven.apache.org/POM/4.0.0">

<modelVersion>4.0.0</modelVersion>

<groupId>epamTask</groupId>

<artifactId>tddJunitDemo</artifactId>

<version>0.0.1-SNAPSHOT</version>

<packaging>jar</packaging>

<name>tddJunitDemo</name>

<url>http://maven.apache.org</url>


-<properties>

<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>

<java.version>1.8</java.version>

<maven.compiler.source>1.8</maven.compiler.source>

<maven.compiler.target>1.8</maven.compiler.target>

</properties>


-<dependencies>

<!-- https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-engine -->



-<dependency>

<groupId>org.junit.jupiter</groupId>

<artifactId>junit-jupiter-engine</artifactId>

<version>5.5.2</version>

<scope>test</scope>

</dependency>

<!-- https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api -->



-<dependency>

<groupId>org.junit.jupiter</groupId>

<artifactId>junit-jupiter-api</artifactId>

<version>5.5.2</version>

<scope>test</scope>

</dependency>

</dependencies>

</project>
