Download Link: https://assignmentchef.com/product/solved-project-2-minivan-doors
<br>
<ul>

 <li>Write a class with multiple methods and a constructor</li>

 <li>Write instance variable (field) declarations</li>

 <li>Write accessor and mutator methods</li>

 <li>Use if statements and boolean conditions</li>

 <li>Write a JUnit test class</li>

</ul>

<strong>Overview</strong>

In this assignment, you will write another complete class that is intended to reinforce your basic skills in writing instance variables, getter methods, and setter methods, while also introducing the use of if statements to provide conditional logic, controlled by boolean conditions based on object state. You will also switch from writing “tester programs” that just print output to writing repeatable, automatically executable software tests for your work using the JUnit testing framework.

The subject of this assignment is inspired by one of the programming exercises from Chapter 5 of the textbook, which is based on the textbook author’s own minivan. If you drive a late model minivan with power doors, you might recognize some of these behaviors yourself.

Your task is to simulate a portion of the control software for the vehicle. You will write a class that represents the state of the controls, providing accessor and mutator methods for the state of the relevant vehicle switches. You will also provide methods that represent door opening actions, and that implement logic matching the description provided below.

<strong>Details</strong>

The textbook author’s minivan has two power sliding doors. Each door can be opened by either a dashboard switch, its inside handle, or its outside handle. However, the inside handles do not work if the minivan’s child lock switch is activated. In order for the sliding doors to open, the gear shift must be in park, <em>and</em> the master unlock switch must be activated. You will write a class that represents these vehicle features, and models the process of deciding whether a sliding door will open or not.

At the same time, you will also write software tests to confirm your solution works the way it should. Instead of writing a “tester” program that just prints out expected results, you will instead write your software tests using the JUnit testing framework, which makes it much easier to repeatedly run and recheck test results as you work.

<strong>Setting Up Your Eclipse Project</strong>

Create a new Java project in Eclipse for this assignment (you might call it “program2”, for example). Then download the following file, which contains library classes we will be using this semester:

Download: <a href="https://sourceforge.net/projects/web-cat/files/Student%20Library/4.14/student.jar/download">student.jar (Links to an external site.)</a>

Once you have downloaded the file, place it in your Eclipse project by dragging it into Eclipse’s window and dropping it on the “program2” project entry in Eclipse’s package explorer view (the tree on the left). When prompted, tell Eclipse to copy the file into the project. Next, right-click on the student.jar file in Eclipse’s package explorer view and choose <strong>Build Path -&gt; Add to Build Path</strong> from the pop-up menu, as shown below. This will make all library classes contained in the file accessible for import/use in your code.

Create a new class in the default package called Minivan and use this for its initial contents (you’ll have to fill in the comments yourself):

// ————————————————————————-

/**

*  Write a one-sentence summary of your class here.

*  Follow it with additional details about its purpose, what abstraction

*  it represents, and how to use it.

*

*  @author your name (your-pid)

*  @version (place the date here, in this format: yyyy.mm.dd)

*/

public class Minivan

{

//~ Fields ……………………………………………………….










//~ Constructor …………………………………………………..




// ———————————————————-

/**

* Creates a new minivan object with the doors closed,

* gear shift in park, child lock switch off, and master unlock

* switch on (unlocked).

*/

public Minivan()

{

/*# Insert your own constructor code here */

}







//~Public  Methods ………………………………………………..




// ———————————————————-

/**

* Replace this with your own comment.

* @return Replace this with your own description.

*/

public boolean pullLeftOuterHandle()

{

// Just a “stub”–a dummy implementation that is just

// enough for the compiler to compile the class. Just

// serves as a placeholder for the real thing, to come later.

return false;

}

}

This is the start of your Minivan class, and already has one method <em>stubbed out</em>–which means there is a very minimal <em>do-nothing</em> implementation of the method, which is just enough to get the method to compile. You’ll see why in a minute.

Create a second class in the default package called MinivanTest and use the text below for its initial contents (you’ll have to fill in the comments yourself). Don’t worry–you’ll be learning what the parts of this file mean throughout this assignment.

// ————————————————————————-

/**

*  Write a one-sentence summary of your test class here.

*  Summarize what your test objectives are.

*

*  @author your name (your-pid)

*  @version (place the date here, in this format: yyyy.mm.dd)

*/

public class MinivanTest

extends student.TestCase

{

//~ Fields ……………………………………………………….




// Holds a minivan object to be used in your individual tests

private Minivan minivan;







//~ Constructor …………………………………………………..




// ———————————————————-

/**

* Creates a new MinivanTest test object.

*/

public MinivanTest()

{

// The constructor is usually empty in unit tests, since it runs

// once for the whole class, not once for each test method.

// Per-test initialization should be placed in setUp() instead.

}







//~ Methods ………………………………………………………




// ———————————————————-

/**

* Sets up the test fixture.

* Called before every test case method.

* Here, we just create a minivan using the default constructor,

* so a freshly created minivan is available for use in each test.

*/

public void setUp()

{

minivan = new Minivan();

}







// ———————————————————-

/**

* Check that the left outside handle does open the door in

* a minivan with the default switch settings.

*/

public void testLeftOuterHandleWithAllSwitchesOff()

{

assertTrue(minivan.pullLeftOuterHandle());

}

}




<strong> </strong>

<strong> </strong>

<strong>Before You Start: Unit Testing in this Assignment</strong>

In this assignment, you’ll begin writing software tests for your work so that you can <em>self-check</em> your code as you write it. Self-checking is an important way for your to confirm your code works the way you expect, and it is really helpful at allowing you to find your own errors as you work.

Sometimes, students with more experience programming aren’t too excited about writing software tests, which is understandable. They can seem a bit boring. However, if you remember back to your math classes or writing classes during your earlier education, you probably recall at least some time you spent checking your own work. In math, when you solve an equation, it is a really good idea to plug the answer you came up with back into the original equation to see if it works. That’s a really strong way to double-check your work to make sure that simple mechanical mistakes (like accidentally flipping a sign, or other small errors) get found <em>right away</em>. Similarly, when writing you’re probably used to repeatedly proof-reading your own words–that is a useful self-checking technique, but it isn’t quite as reliable as “plugging the answer back into the original”, because there’s no definitive way to tell if your proof-reading found all the problems. Still, you do it because it helps improve the quality of your work.

So, software testing the way we’re going to practice it in this class amounts to the same thing: it is your way of <em>self-checking</em> your own work to find mistakes. Further, if you self-check each piece of your code <em>as you write it</em> you’ll find more errors faster. If you write all your code first, and save all the self-checking for the end, your self-checking won’t find as many errors. Worse still, when you find a problem, you may not know exactly <em>where</em> in your assignment the problem is, and it can take a lot longer to locate the cause of the mistake and fix it. Generally speaking, if you test your own code as you write it, you’ll find more errors faster, and save more time later compared to saving software testing (i.e., self-checking) until the end after your entire assignment is complete. So <em>please write software tests for each method, <u>as</u> you write that method</em> rather than saving testing for the end.

OK, with that out of the way, you need to know how to write software tests. Software tests work best when they are short and focused–focus on testing one single thing at a time. We’ll be writing our software tests as individual methods. Each test (each method) will have a very simple structure with three main steps, like this:

public void testSomething()

{

// 1. Set up initial conditions for your test




// 2. Perform the action you want to test




// 3. Check that it behaved as you expected

}

For example, the initial contents shown above for the Minivan class include a stub for a method called pullLeftOuterHandle() that represents pulling on the outside door handle of the left sliding door on the minivan. This action <em>might</em> open the door, and the method is supposed to return true if it does, or false if the door remains closed. Suppose we want to test this method in a minivan where all the switches are “off”. We could do this as follows:

<ol>

 <li>Create a new minivan. A new minivan has all the switches in their default positions, so that’s all we need to do.</li>

 <li>Pull the left outer door handle.</li>

 <li>Check that the door really did open.</li>

</ol>

In code, it might look like this:

public void testLeftOuterHandleWithAllSwitchesOff()

{

// 1. Set up initial conditions for your test

Minivan minivan = new Minivan();




// 2. Perform the action you want to test

boolean result = minivan.pullLeftOuterHandle();




// 3. Check that it behaved as you expected

assertTrue(result);

}

Note that this method has a name that starts with “test”. This is a convention, but it also allows JUnit to recognize your test methods easily. If you don’t want to use names that start with “test”, you can instead use the @Test annotation as shown in the textbook.

The first step in the test method shown above, which involves setting things up in the situation you want to test, is just plain old Java. Just create the objects you need, and call whatever methods are necessary to put them in the state you want them in for your test.

Note that setting up the “starting state” for tests is such a common thing, there’s also a shorthand. In the provided text for the MinivanTest class above, you’ll see the class actually declares a <em>field</em> called minivan instead of using a local variable. It also provides a method called setUp() that initializes the field. These two go together to perform step (1) for many of your tests. JUnit will automatically invoke the setUp() method (if you have one) before every single test is executed. That makes it a great place to put common initialization actions you want to happen before each and every test–and a great place to put code for step (1), so you don’t have to repeat that code in every single test method. That’s why the version of the test provided earlier doesn’t even include a step (1)–that step was placed in setUp() instead.

The second step involves calling the action you want to check. It’s pretty easy, since it is usually just a method call. In fact, it is so short that often times it might even be combined with step (3). However, for every test, it should be clear to you that there is one specific method call inside the test that is the “thing being tested”.

The third step is to check your work! That is, check that the method you’re testing did what it is supposed to do. In some cases, the method may simply return a result. In that case, all you have to do is make sure the correct result is returned. In other cases, the method might <em>change</em> the object you’re working with. Then you’d need to call one (or more) accessors to check that the object changed appropriately.

In either case, the tool you’ll use to check that something happened the way you expected are <strong>assert methods</strong>. These are utility methods provided by JUnit just for the purpose of checking results, and they typically have names that start with “assert”. The three you might use in this assignment are:

<table>

 <tbody>

  <tr>

   <td width="623">

    <table>

     <thead>

      <tr>

       <td><strong>Method</strong></td>

       <td><strong>Meaning</strong></td>

      </tr>

     </thead>

     <tbody>

      <tr>

       <td>assertEquals(<em>expected</em>, <em>actual</em>);</td>

       <td>Assert that two values are equal, using the equals(Object) method to compare them. This is the most commonly used assert method in your arsenal.</td>

      </tr>

      <tr>

       <td>assertTrue(<em>condition</em>);</td>

       <td>Assert that a boolean <em>condition</em> is true.</td>

      </tr>

      <tr>

       <td>assertFalse(<em>condition</em>);</td>

       <td>Assert that a boolean <em>condition</em> is false.</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

Note that if there are two parameters, the <strong>expected value always comes first</strong> and <strong>the value you are checking always comes second</strong>.

To <strong>run</strong> your tests, right-click on your MinivanTest class in the package explorer view and choose <strong>Run As -&gt; JUnit Test</strong>.

Eclipse will run all your tests and show you the results. Here, we <em>expect</em> our first test to fail, since we haven’t implemented anything yet and just have a stub. Eclipse will show your JUnit results in a view that looks like this:

OK, so now you have a Minivan class ready, and a MinivanTest class that’s also ready. Our advice for this assignment is to do the following:

<ol>

 <li><strong>Read</strong> through the requirements for the Minivan class so that you understand what it is supposed to do.</li>

 <li><strong>Plan the order</strong> in which you want to implement the minivan’s methods.</li>

 <li><strong>Implement methods one at a time</strong> according to your plan. Feel free to adjust your plan as you need to. However, focus on writing one method at a time.</li>

 <li><strong>Test each method as you write it.</strong> Write your tests as you write each individual method. Some students find it useful to <em>write a stub of their method first</em> so they can write their tests before they actually do the implementation. The stub allows your tests to compile, even though initially they’ll all fail. This strategy goes by the name of <strong>test-first</strong></li>

</ol>

<h3>The Requirements for the Minivan</h3>

Write a class called Minivan that models the door-opening behavior of our minivan. Your class should provide the following methods (you define the instance variables/fields you need):

Minivan()

This default constructor initializes the van so that the child lock switch is off (deactivated), the master unlock switch is on (activated), and the gear shift is in park.

getChildLock()

A boolean accessor method that returns the state of the child lock switch as a boolean value (false == off and true == on).

setChildLock(boolean value)

A setter method that turns the child lock switch on or off.

getMasterUnlock()

A boolean accessor method that returns the state of the master unlock switch as a boolean value (false == off and true == on).

setMasterUnlock(boolean value)

A setter method that turns the master unlock switch on or off.

getGearShiftPosition()

An accessor method that returns the position of the gear shift as a single char value, which is one of: ‘P’, ‘R’, ‘N’, ‘1’, ‘2,’ ,’3′, or ‘D’.

setGearShiftPosition(char value)

A setter method that sets the gear shift position. Expected values are one of: ‘P’, ‘R’, ‘N’, ‘1’, ‘2,’ ,’3′, or ‘D’. You may assume that only one of these values will be passed in (you are not required to verify that only legal values are used in this method for this assignment).

pullLeftOuterHandle()

A method that represents pulling the outside handle of the left sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

pullLeftInnerHandle()

A method that represents pulling the inside handle of the left sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

pullLeftDashSwitch()

A method that represents pulling the dashboard switch for the left sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

pullRightOuterHandle()

A method that represents pulling the outside handle of the right sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

pullRightInnerHandle()

A method that represents pulling the inside handle of the right sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

pullRightDashSwitch()

A method that represents pulling the dashboard switch for the right sliding door, assuming the door is already in the closed position. This method returns a boolean value indicating whether the door opens (true) or remains closed (false). We will assume the door is returned to the closed position by the vehicle’s operator before the next method is called.

<h3>A Word about Design</h3>

For this assignment, you’ll notice that there are some features that are repeated (perhaps with minor variations) in the Minivan class. If you review the program grading rubric for this course, you will notice that “repeated code” is one of a number of design weaknesses that can cause your solution to receive lower ratings. When you discover these sections of repeated code, consider creating your own “helper” method(s) so that you can write such code once, and simply call it in multiple places instead of repeating it.

Also, as you test your code, you may find that Web-CAT indicates you have logical conditions (if statements) that are not being thoroughly tested. When you have multiple conditions combined with &amp;&amp; or ||, make sure you include separate tests for each unique way the condition can succeed or fail. For example, if you have an if statement that includes a condition like (isHappy || !isBusy) remember that there are <em>3 separate</em> ways the condition can be determined. First, if isHappy is true, the condition will also be true. However, if isHappy is false, there are <em>two more</em> possibilities (either isBusy is true, or isBusy is false). You’ll need to test all three possibilities for an if statement with this kind of condition in order to get full credit. In general, if there are <em>K</em> basic conditions or comparisons in an if statement, then there are <em>K + 1</em> test cases needed to cover all the possibilities (in this example, 2 basic conditions means 3 separate test situations). Web-CAT will highlight conditions you haven’t fully tested, but it won’t tell you which possibilities you missed–you have to figure that out yourself, based on the tests you have written.

<h3>Submit to Web-CAT</h3>

Submit your solution to Web-CAT (<a href="http://web-cat.cs.vt.edu/">http://web-cat.cs.vt.edu (Links to an external site.)</a>), once a message has been posted to Piazza that Web-CAT is ready for Program 2. Read through the feedback that Web-CAT provides and fix any problems it points out.

Look carefully at your feedback. In the summary, you will see a table listing each of your source files with a green/red bar by each non-test file. <strong>If the bar for any file is not completely green</strong>, then some code in that file was not exercised by your tests. Click on the file name to view the source code for your file and <strong>look for lines that are highlighted in a salmon color</strong>. Hover your mouse over highlighted lines for additional information. <strong>Add test cases to exercise the code that is highlighted</strong>. This may require you to test methods in situations other than those you’re already testing.

Feel free to improve and resubmit your code as many times as you like before the deadline in order to improve your score. Please post on the Piazza forum if Web-CAT complains about any issue in your code’s formatting that you do not understand how to fix, and we’ll be happy to explain.

Remember that projects in this course will be partially evaluated by Web-CAT (35 points for reference tests, 15 points for style) and partially by human evaluation (50 points). Therefore, Web-CAT’s automated score will be at most 50/100 points. See the <a href="https://vt.instructure.com/courses/25917/pages/program-grading-rubric">program grading rubric</a> for full details on the grading criteria applied to this assignment.


