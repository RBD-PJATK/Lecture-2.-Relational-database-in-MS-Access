# Lecture 2. Relational database in MS Access

<hr><h3>Abstract</h3>

<p>Lecture 2 presents an implementation of the relational data model.
It is <i>Microsoft Access</i>, which is a simple database system.
MS Access offers facilities to design tables (in <i>the design view</i>)
as well as to browse and edit the data in these tables (in <i>the datasheet view</i>).
The same applies to <i>views</i> of MS Access (they are called <i>queries</i> here).
One designs them in <i>the design view</i> and uses them in <i>the datasheet view</i>.</p>

<p>While you are reading the lecture, please make exercises as they appear.
After you finish reading the lecture, please do
<a href="#Zadania"> exercises 1, 2, 3 and 4</a>.  When you complete them, you will have the database 
for a library.  You need MS Access to solve these exercises.</p>
 
<hr><h3><a name="Program">MS Access</a></h3>

<p>MS Access is the MS Office package which:

<ol>
<li>is able to create a database consisting of tables and views (queries);
<li>has a graphical user interface for the objects of the database (tables and views);
<li>has a graphical user interface for database applications (forms, reports, web pages);
<li>contains the developer environment to code database application
	(macros, VBA - Visual Basic for Applications and SQL - Structured Query Language).
</ol>

<hr><h3><a name="Tabele">Tables in MS Access</a></h3>

<p>Tables in MS Access are:

<ol>
<li>logical structures to store data in the database,
<li>the source of data for other objects like queries, forms and reports,
<li>an element of the graphical user interface.
</ol>

<hr><h3><a name="Projekt">Designing tables</a></h3>

<p>The designer of the database defines the schema of a table in <i>the design view</i>.
This schema includes the names of the columns (fields)
which will store the rows of this table.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_1.png"></p>

<hr><h3><a name="Arkusz">Datasheet</a></h3>

<p>After you have defined the schema of the table, you can enter data and browse through it in
<i>the datasheet view</i>.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_4.png"></p>

<p>In the datasheet view you can perform the following operations on the rows of the table:</p>

<ol>
<li>browse through the rows;
<li>search particular rows (i.e. to filter them);
<li>add a new row;
<li>delete an existing row;
<li>edit the values of an existing row.
</ol>

<hr><h3><a name="Okno">The database window</a></h3>

<p><i>The database window</i> is the first window you see when you open a database.  
This window displays the list of the objects of the database and
offers the following operations on tables:</p>

<ol>
<li>creating a new table (press the button <b>New</b>),
<li>switching to the design view of an existing table (press the button <b>Design</b>),
<li>switching to the datasheet view of an existing table (press the button <b>Open</b>),
<li>removing an existing table (press the icon <b>Delete</b>),
</ol>

<p>Create tables <i>Employees</i>, <i>Cases</i> and <i>Letters</i> in 
the same way as we created the table <i>Customers</i>. 
The objects will be displayed in the database window.
</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_6.png"></p>

<p>It is time for a short question which checks whether you remember all kinds of objects 
available in the user interface of a relational database in MS Access.</p>

<table border="0">
<tr><td class="notec">
<a href="javascript:popUp('ok1.html',400,150)">Is</a> it true that
the database window of MS Access shows only tables and views?</table>


<hr><h3><a name="Typy">Data types of MS Access</a></h3>

<ul>
<li><b>Text</b> - strings up to 255 characters.
<li><b>Memo</b> - long texts (u to 64000 characters),
<li><b>Number</b> - byte, integer, long integer, single or double.
<li><b>Data/Time</b> - e.g. &quot;22.06.97&quot;, &quot;22.06.97 12:12:34&quot;.
<li><b>Currency</b> - e.g &quot;$200.25&quot;.
<li><a name="Autonumer"><b>Autonumber</b></a> - numbers increased automatically for each new record
	or generated randomly.
<li><b>Yes/No</b> - logical values.
<li><b>OLE Object</b> - e.g. image, Word document, Excel spreadsheet or other object handled
	by a Windows application.
<li><b>Hyperlink</b> - the address of a web document (the name of a file, or URL of a web page).
</ul>

<hr><h3><a name="Kreator">Lookup wizard</a></h3>

<p>When you define a field, you can use a special option available in the combo box
which offers the choice of the type.
It is the <b>Lookup Wizard</b>.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_2.png"></p>

<p>The lookup defines the list of values or indicates a column of a table (or a query)
which
will be the source of values for the field, e.g. the values of the foreign key are taken
from the column of the primary key.  The field which has the lookup is displayed as a combo box.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_5.png"></p>

<p>In the datasheet view it is better to show the values associated with the lookup and not the field of lookup itself.
Instead of <i>Empno</i>s of employees you can show their names (in the pop-down list and in the field).</p>

<p>The values displayed in the field <i>Empno</i> 
(in the table <i>Cases</i>) are drawn from the table
<i>Employees</i>.  The <i>Empno</i> is not shown, because the width of this column is set to zero.
However, the database physically stores the identifiers of employees, i.e. values of field <i>Empno</i>.
</p>


<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_7.png"></p>


<hr><h3><a name="Kol">Properties of columns</a></h3>

<p>Apart from the data type and the description (meaning) of a column, you can also set other properties
of this column.  Some of them may be perceived as <i>integrity constraints</i>:</p>

<dl>
<dt><b>Field Size</b>
<dd>Self explanatory.
<dt><b>Validation Rule</b>
<dd>For example <code>&gt; 100 And &lt; 5000</code> for salaries or <code>Like "K???"</code> for names.
<dt><b>Required</b>
<dd>Do you have to enter a value into this column?  (Is <code>Null</code> allowed here?)
<dt><b>Allow Zero Length</b>
<dd>Can a value in this column be the empty string? (applies to data types <i>Text</i> and <i>Memo</i>).
</dl>

Others provide additional information for the graphical user interface:

<dl>
<dt><b>Format</b>
<dd>How to display the value?
<dt><b>Decimal Places</b>
<dd>How many decimal places to display? (applies to numerical columns only).
<dt><b>Input Mask</b>
<dd>Characters shown during data entry.
<dt><b>Caption</b>
<dd>The name of this field in forms and reports. 
<dt><b>Default Value</b>
<dd>The value to be inserted automatically when the user does not provide it.
<dt><b>Validation Text</b>
<dd>The message to be displayed when the user breaks the <b>Validation Rule</b>.
<dt><b>Indexed</b>
<dd>Is this column indexed?
</dl>

<hr><h3><a name="Tab">Integrity constraint for a table</a></h3>

<p>The integrity constraints for more than one column are defined in
windows "Table Properties"
(select menu item "View -&gt; Properties" or button "Properties" on the toolbar).  
We want to stress
that the customers cannot use more credit than the established limit.  Thus we define "Validation Rule"
to be <code>[Credit used] &lt; [Credit limit]</code>. We also set the appropriate error message.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_8.png"></p>

<hr><h3><a name="Indeksy">Indexes</a></h3>

<p><i>An index</i> accelerates the search for records which have a given value in one or more fields.
In order to work with indexes, select the menu item "View -&gt; Indexes"
or the button "Indexes" on the toolbar.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_10.png"></p>

<hr><h3><a name="Zmiana">Change of the schema of a table</a></h3>

<p>You can change the schema of a table by means of the same facilities of the graphical 
user interface which were used to create a table.  You can:</p>

<ul>
<li><b>add a new field</b>,
<li><b>remove a field</b> (do not forget to remove it also from queries, forms and reports!),
<li><b>rename a field</b> (do not forget to rename it accordingly in queries, forms and reports!), 
<li><b>change the data type of a field</b>.<br>

	It causes the conversion of all the stored data. 
	You can increase the size, change <code>Text</code> to <code>Memo</code> etc. 
	If the system is unable to convert the data correctly, you have two choices:
	to abandon the change of the data type or to replace erroneous data items with <code>Nulls</code>.	
</ul>


<p align="center"><table border="0"><tr><td class="notec"><a href="javascript:popUp('ok3.html',500,180)">Is</a>
it true that MS Access provides a uniform interface to edit the schema of a table and to view the rows of this table?
</table>

<p>We suggest solving <a href="#Zadanie 1">exercise 1</a> now.</p>

<hr><h3><a name="Powiazania">Relationships between tables</a></h3>

<p>When you design the schema of a database, you should also plan the <i>associations</i>
(<i>relationship</i>, <i>relations</i>) between the tables. Since in the field of databases
the term <i>relation</i> is understood as a mathematical abstraction of a table, we will use the term
<i>association</i>.

<p>Here are the possible purposes of associations between tables.</p>

<ul>
<li><b>To enforce referential integrity</b> between tables (the systems cares
	about it).
<li><b>To automatically create the join condition</b> between tables in a query. 
<li><b>To synchronize the display of related data</b> in forms, e.g. the form with orders
	automatically displays the orders of the customer selected on the form with customers
	(it also applies to subreports).
</ul>

The related fields must fulfill the following conditions.

<ul>
<li>The referenced field(s) of a table must constitute its primary key or there must be
	a unique index created for them.
<li>The referenced table is called <i>the master</i>, while the referencing table is 
	called <i>the detail</i>.
<li>The associated fields must have the same data type.
</ul>

<hr><h3><a name="Diagram">Relationship diagram</a></h3>

<p>You can model and view the schema of the database on the relationship diagram.
In order to open it, choose the menu item "Tools -&gt; Relationships".</p>

<p>Frames represent <i>tables</i>, while the lines between the frames are
the associations (relationships) between tables.</p>

<table><tr><td class="przyk">
On the diagram below the association between <i>Letters</i> and 
<i>Cases</i> is selected and the window with its properties is displayed 
(window "Edit Relationships").
</table>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_9.png"></p>

<p>Every association between tables has two ends: the master and the detail.
The master is marked with number "1" placed near the referenced table.
The detail is marked with the symbol of infinity placed near the referencing table.</p>

<p>Every association can be written down as two sentences which describe
the relationship between associated objects. Here is the full statement
of the schema presented above:</p>

<table><tr><td  class="przyk">
<p>Each letter concerns exactly one case. Each case can be discussed in many letters.</p>
<p>Each case is submitted by exactly one customer. Each customer can submit many cases.</p>
<p>Each case is handled by exactly one employee.  Each employee can handle many cases.</p>
</table>

<p>Please answer a simple question</p>

<table><tr><td class="notec"><a href="javascript:popUp('ok4.html',500,140)">
Is</a> it true that MS Access shows the schema of the database 
in window "Relationships"?</table>

<p>and make a simple exercise.</p>

<table><tr><td class="notec"><p> <a href="javascript:popUp('ok5.html',400,100)">
Divide</a> the following terms into two groups of related items:
<i>"one"</i>, <i>detail table</i>, <i>primary key</i>, <i>"many"</i>,
<i>master table</i>, <i>foreign key</i>.
</table>

<hr><h3><a name="Ref">Referential integrity</a></h3>

<p>When you define an association between tables, you have to choose
option "Enforce referential integrity".</p>

<ul>
<li>When we insert a new record into the detail table and this record has
	a non-empty value of the foreign key, then in the master table
	there must exist a row with this value of the primary key, e.g. if
	we insert a case with the identifier of a customer, this identifier
	must also be present in table <i>customers</i>.  This identifier 
	can also by <code>Null</code>.
<li>You cannot delete a record from the master table which is referenced
	by some records in the detail table. For example, you cannot delete
	<i>a customer</i>, if there are <i>cases</i> submitted by this
	customer. 
<li>If you set option <i>Cascade Delete Related Records</i>,
	the deletion of a record from the master table causes
	automatic deletion of all related records from the detail table.
<li>If you set option <i>Cascade Update Related Fields</i> the update of the
	primary key of a record of the master table causes automatic
	update of the values of the foreign key in related records
	of the detail table.
</ul>

<hr><h3><a name="Typ">Join types</a></h3>

<p>The results of queries based on associated tables depend
on the chosen <i>type of join</i>.  There are three types of joins. The first of them
is the default.</p>

<dl>
<dt><i>Inner join</i>
<dd>Only include rows where the joined fields from both tables are equal.
	For example, if a customer has submitted no cases, she will not be displayed.

	<p align="center"><img border="0" src="images/2_12.png"></p>
 	<p align="center"><img border="0" src="images/2_18.png"></p>

<dt><i>Right outer join</i>
<dd>Include ALL records from the right table and only those records from the
	 left table where the joined fields are equal.
	For example, a <i>customer</i> who submitted no <i>cases</i>
	will be displayed, but the <i>a case</i> not associated with any
	<i>customer</i> will not be displayed.

	<p align="center"><img border="0" src="images/2_20.png"></p>
	<p align="center"><img border="0" src="images/2_19.png"></p>

<dt><i>Left outer join</i>
<dd>Include ALL records from the left table and only those records from the
	right table where the joined fields are equal.
	For example, a <i>case</i> not associated with any
	<i>customer</i> will be displayed, but a <i>customer</i>
	who submitted 
	no <i>cases</i> will not be displayed.

	<p align="center"><img border="0" src="images/2_21.png"></p>
</dl>

<p>We suggest solving <a href="#Zadanie 2">exercise 2</a> now.</p>

<hr><h3><a name="m">Queries</a></h3>

<p>In MS Access <i>a query</i> is either:</p>

<ul>
<li><i>a view</i> (called <i>a select query</i>),
<li><i>a data manipulation</i> (called <i>a functional query</i>), e.g.
	creation of a table, update of rows.
</ul>

<h4><a name="Kwerenda">Select query</a></h4>

<p>The result of the execution of a select query is a <i>dynamic record set</i>. 
It has the form of a table, but it is not stored in the database persistently.
It is displayed as a datasheet just like tables.</p>

<h4><a name="o">Methods to create queries</a></h4>

<ol>
<li>the query grid (the graphical method),
<li>SQL statement,
<li>VBA code.
</ol>

<p>Methods 2 and 3 will be presented during further lectures.</p>

<h4><a name="Siatka">Query grid</a></h4>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_11.png"></p>

<p>The result of the execution of a select query is a datasheet just like for tables.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_18.png"></p>

<p>The join type is set separately for each select query, although initially it 
is set to the default type defined in window "Relationships".</p>

<p>When we create a query, we choose its type from menu "Query".  The default type
is "Select Query".  After the type is chosen,  MS Access adjust the query grid appropriately
by adding or removing its rows.</p>

<h4><a name="Usuw">Delete query</a></h4>

<p><i>A delete query</i> causes the deletion of rows which
fulfill the specified condition, e.g.

<pre>((Empno &gt; 100 AND Sal &lt; 1000) OR Empno &lt; 10)</pre>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_15.png"></p>

<h4><a name="Dol">Append Query</a></h4>

<p><i>An append query</i> causes the insertion of rows into a table. For example, the following query inserts
the row: <code>(3244, 'Kelly', 'Analyst')</code> into table <i>Employees</i>.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_16.png"></p>

<p>We can name a table in row "Table" of the query grid.  If we do so,
the rows selected from this table will be appended
to the target table.</p>

<h4><a name="Akt">Update Query</a></h4>

<p><i>An update query</i> updates rows of a table, e.g. we can raise
the salaries of employees who earn less than 500 by 10%.</p>

<p align="center"><img border="0" src="https://gakko.pjwstk.edu.pl/materialy/2398/lec/wyklad02/images/2_17.png"></p>

<p>We suggest solving <a href="#Zadanie 3">Exercise 3</a> now.</p>

<hr><h3><a name="Podsumowanie">Summary</a></h3>

<p>In lecture 2 we presented the graphical user interface to a relational database run by MS Access.  In this interface
a table can be manipulated in two views. <i>The design view</i> is used to design the schema of the table,
while <i>the datasheet view</i> is used to browse and edit the data of the table. In MS Access the rows are called
<i>records</i>. In <i>the datasheet view</i> you can browse records, filter them, add new ones and update or delete
existing records.</p>

<p>Window <i>Relationships</i> is used to edit the properties of associations between tables and to set
<i>the referential integrity constraints</i> and the <i>join types</i> of each association.</p>

<p>In MS Access views are called <i>select queries</i>.
There are also queries which perform operation on data.  They are
<i>append queries</i>, <i>update queries</i> and <i>delete queries</i>. Queries like tables can be manipulated in two views.
<i>The design view</i> is used to define the query, i.e. to set its base tables, join conditions and the operations to be performed.
<i>The datasheet view</i> is used to browse and edit the returned rows.  In the datasheet view of a 
query you can also add new records and update or delete existing ones.</p>


<table><tr><td class="notec">

<p> <a href="javascript:popUp('ok2.html',320,170)">
Pair</a> terms which mean the same in MS Access:
<i>association</i>, <i>column</i>, <i>field</i>, <i>record</i>, <i>relation</i>, <i>relationship</i>,
<i>row</i>, <i>select query</i>, <i>table</i>, <i>view</i>.
</table>

<p>We suggest solving <a href="#Zadanie 4">Exercise 4</a> now.</p>

<hr><h3><a name="Slownik">Dictionary</a></h3>

<dl>

<dt><a href="#Powiazania">association</a> (relationship, relation) 
<dd>A relationship between two tables. A record of first table references the associated 
	record of the second table, e.g. the record of an employee contains a reference
	to the record of the department where the employee works. 

<dt><a href="#Autonumer">autonumber</a>
<dd>The data type of numbers increased automatically for each new record or generated randomly.
	It may be used as the primary key or, less often, as a unique key.

<dt><a href="#Okno">database window</a>
<dd>The window of MS Access which shows all objects of the database.

<dt><a href="#Arkusz">datasheet view</a>
<dd>The graphical interface of MS Access which displays the content of a table
	and performs operations on its rows.

<dt><a href="#Projekt">design view</a>
<dd>The graphical interface of MS Access that facilitates the design of the schema of a table.

<dt><a href="#Indeksy">index</a>
<dd>A data structure built for a column or a set of columns which accelerates
	searches for records with the given values in these columns.

<dt><a href="#Typ">join type</a>
<dd>The method to join rows from two tables.  It states what to do with 
	records which do not have their counterparts in the other table.
	If the join is <i>inner</i>, such rows are not displayed.
	If the join is <i>outer</i>, such rows belong to the result.

<dt><a href="#Kreator">lookup</a>
<dd>The pull-down list of values to be inserted into a given field.
	It may contained hard-wired values or values taken from a table
	of the database.

<dt><a href="#Program">MS Access</a>
<dd>The program sold by Microsoft which offers graphical user interface for
	relational databases.  It can be used to design the schemata of tables
	(in the design view) and to perform operations on their rows
	(in the datasheet view).

<dt><a href="#m">query</a>
<dd>Either a view (a select query) or a statement of data manipulation, e.g.
	creation of a new table, update of existing rows.

<dt><a href="#Siatka">query grid</a>
<dd>The graphical interface of MS Access which facilitates the design of a query.

<dt><a href="#Ref">referential integrity</a>
<dd>The guarantee that when the rows of table <i>A</i> reference rows of table
	<i>B</i> (<i>A</i> is the detail while <i>B</i> is the master),
	for each row of table <i>A</i> the referenced row of table <i>B</i> exists.
<dt><a href="#Diagram">relationship diagram</a>
<dd>The graphical representation of the associations among the tables of a database.
	Frames represent <i>tables</i>, while the lines between the 
	frames are the <i>associations</i> between tables.
</dl>

<hr><h3><a name="Zadania">Exercises</a></h3>

<h4><a name="exercise-info">Information</a></h4>

<p>Points labeled with asterisks require more effort.</p>

<h4><a name="Zadanie 1">Exercise 1</a></h4>

<p>Build a table which will store the information on your own books. The table will be used to search
books from the given field (e.g. <i>Computer science</i>), on the given subject (e.g. <i>Data warehouses</i>) or
of a given author. You will also check whether the book is lent, who has
borrowed it and how to contact this person.
You will search for the translators and authors of books as well as their contact addresses.
</p>

<ol>
<li>Start MS Access and open the database window of a new database.
<li>Select tab "Tables" and press button "New".  Then choose "Design view".
<li>Create table <i>Books</i> with appropriate columns and their data types.
	You can Use table <a href="biblio.html" target="_blank">bib</a> as a stencil.
	Do not forget to set the primary key (menu item "Edit -&gt; Primary key").
<li>Enter sample data (select "View -&gt; Datasheet view).
<li>Make sure that you know how to perform basic operations on tables in the datasheet view.
	(use menus, the toolbar and the pop-up menu). 

<ul>
<li>Enter a new record (Insert -&gt; New Record).
<li>Delete the current record (Edit -&gt; Delete Record).
<li>Update the current record.
<li>Sort the records according to the current column (Records -&gt; Sort).
<li>Add a new column (Insert -&gt; Column).
<li>Change the name of a column (Format -&gt; Rename Column).
<li>Delete a column (Edit -&gt; Delete Column).
<li>Search data in the table (Edit -&gt; Find...). You can use wild cards: <code>*</code> means any string of characters;
	<code>?</code> = any characters; <code>#</code> = any digit.
<li>Replace the data of the table (Edit -&gt; Replace...).
<li>Filter records, i.e. select a subset of records which fulfill the given condition
	(Records -&gt; Filter):
	<ul>
	<li>-&gt; Filter By Selection (according to the value in the current field).
	<li>-&gt; Filter By Form (select appropriate values in the pop-up form).
	</ul>
<li>Apply the filter set before (Records -&gt; Apply Filter/Sort).
<li>Display all record (Records -&gt; Remove Filter/Sort)
</ul>


<li>Save the content of the table as (File -&gt; Save As...):
	<ul>
	<li>text file,
	<li>Word document (use tool "Publish It With MS word"),
	<li>Excel spreadsheet (use tool "Analyze It With MS Excel"),
	<li>HTML document.
	</ul>
<li>Explain the drawbacks of this schema which consists of one big table.
</ol>


<h4><a name="Zadanie 2">Exercise 2</a></h4>


<p>Build a new database which stores the same information as in <a href="#Zadanie 1">exercise 1</a>, however:
	<ul>
	<li>the data on each kind of objects should be stored in a separate table;
	<li>each field should contain an atomic (indivisible) value;
	<li>there should be no redundancies.
	</ul>
</p>

<ol>
<li>Create all necessary tables.  Define their primary keys. Remember that the values of the primary keys
	will be used as the values of foreign keys. This is why one usually creates an additional column
	to be the artificial identifier of records. Its data type is <i>Autonumber</i>.
<li>Create columns of the foreign keys by means of the Lookup Wizard.
<li>Connect the tables with relationships (menu item "Tools -&gt; Relationships"). Enable the referential
	integrity. Align the tables so that the lines of relationships do not cross.
<li>Enter data on at least fifty of your books.
</ol>

<h4><a name="Zadanie 3">Exercise 3</a></h4>

<p>Using the query develop the following queries.  Define parameters if they are necessary.</p>

<ol>
<li>List the titles of all your books.
<li>List the first names and the last names of all persons stored in your database.
<li>List the first names and the last names of all authors of books.  Do not display duplicates
	on this list (set the query's property "Unique Records" to "Yes").
<li>List (without duplicates) the first names and the last names of all translators of books.
<li>List (without duplicates) the first names and the last names of all
	persons who have borrowed
	at least one of your books.
<li>Given the subject (as a parameter) list all books on this subject.
<li>Given the title of a book list the first names and the last names of its authors.
<li>Given the first name and the last name of an author, list all books written by this author.
<li>List all borrowed books together with the second name and the address of the borrower.
<li>List all books whose author is also the translator.
<li>Display the number of books.
<li>List all authors and for each author give the number of her books.  Sort the result
	according to this number.
<li>List the subjects, together with the number of books on this subject.
<li>List the fields, together with the number of domain in this field.
<li>List the fields, together with the number of books from this field.
<li>List authors who have written books on at least two different subjects.
<li>List authors who have written books from at least two different fields.
<li>List persons who have borrowed at least two books.
<li>Remove the given book from the database (use a parameterized query).
<li>Add a new author to the database (use a parameterized query).<br>
	<u>Warning</u>: In order to add a single row, you have to use a temporary table
	with one row. MS Access requires that two tables are specified: one as the source,
	and the other as the destination. Values in Autonumber fields are set automatically.
<li>Publisher "WNT" changes its name to "NT Press". Appropriately update the name of the publisher
	in all related books. 
<li>**
	<br>Use an append query and <i>linked tables</i> (menu item "File -&gt; Get External Data -&gt; Link Tables...)
	to develop a back-up facility.
	<p><ol type="a">
	<li>Create a separate database, e.g. <code>copy.mdb</code>.
	<li>Link your tables in this new database.
	<li>Create append queries which copy the contents of the original tables to the local tables.
	</ol></p>

	<p>What will happen if you try to run these append queries again?
	How to design such back-up facility properly to be run daily? </p>
</ol>

<h4><a name="Zadanie 4">Exercise 4</a></h4>

<p>Give an example of an application domain in your environment such
that it is worth developing
a database for it.  The database is to be understood as a set of objects: tables, select queries, forms,
reports and subprograms (functional queries, macros and procedures). List the objects that can be useful.
For a while neglect the event procedures and the integration of the objects into an application.
</p>
