# 👋 Hi friends! I'm Sahil.

I'm a MTech CS Student @IIT Kharagpur and I write articles @Neuronize(https://neuronize.dev/') and @Computize(https://computize.dev/'). 


### 📙 Blog Posts
<!-- BLOGPOSTS:START -->
 <img src="$cover_image" alt="Cover Image" width="200" height="200" align="left">

## [Mastering Python Function Arguments: A Comprehensive Guide](https://neuronize.dev/mastering-python-function-arguments-a-comprehensive-guide)

&lt;p&gt;Mastering Python function arguments is crucial for any programmer looking to elevate their skills in this versatile language. This comprehensive guide will walk you through the intricacies of parameters and arguments, their differences, and how to effectively use positional and keyword arguments. Additionally, you&#39;ll learn about unpacking iterables, leveraging &lt;em&gt;args and&lt;/em&gt; *kwargs, and how to bring it all together for cleaner and more efficient code. By the end of this guide, you&#39;ll have a solid understanding of Python function arguments and be well-equipped to tackle complex programming tasks.&lt;/p&gt;
&lt;h2 id=&quot;heading-parameters-vs-arguments&quot;&gt;Parameters vs Arguments&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we define a function &lt;code&gt;my_func&lpar;a, b&rpar;&lt;/code&gt; and it&#39;ll receive two values &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In this context &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; are called parameters of &lt;code&gt;my_func&lpar;&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, when we define a function, the things that are inside the parentheses are known as parameters.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;When we call the function, the things that are inside the parentheses are known as arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, let&#39;s say we created two variables &lt;code&gt;x = 10&lt;/code&gt; and &lt;code&gt;y = &#39;a&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, we call the &lt;code&gt;my_func&lpar;x, y&rpar;&lt;/code&gt; function. Here &lt;code&gt;x&lt;/code&gt; and &lt;code&gt;y&lt;/code&gt; are arguments of the function &lt;code&gt;my_func&lpar;&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-positional-and-keyword-arguments&quot;&gt;Positional and Keyword Arguments&lt;/h2&gt;
&lt;h3 id=&quot;heading-positional-arguments&quot;&gt;Positional Arguments&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;The most common way of assigning arguments to parameters is via the order in which they are passed i.e. their position.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Suppose, we defined a function &lt;code&gt;my_func&lpar;a, b&rpar;&lt;/code&gt; with parameters &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;While calling the function, if we write &lt;code&gt;my_func&lpar;10, 20&rpar;&lt;/code&gt;, then 10 will assign to the variable &lt;code&gt;a&lt;/code&gt; i.e. &lt;code&gt;a = 10&lt;/code&gt; and 20 will assign to the variable &lt;code&gt;b&lt;/code&gt; i.e &lt;code&gt;b = 20&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;If we call the function &lt;code&gt;my_func&lpar;20, 10&rpar;&lt;/code&gt;, then 20 will assign to &lt;code&gt;a&lt;/code&gt; i.e &lt;code&gt;a = 20&lt;/code&gt; and 10 will assign to &lt;code&gt;b&lt;/code&gt; i.e &lt;code&gt;b = 10&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}, c={2}&quot;&lt;/span&gt;.format&lpar;a, b, c&rpar;&rpar;

my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT --------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;h3 id=&quot;heading-default-values&quot;&gt;Default Values&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;A positional argument can be made optional by specifying a default value for the corresponding parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we define a function &lt;code&gt;my_func&lpar;a, b = 10&rpar;&lt;/code&gt;, this is how we specify a default value.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, we are saying if the user/function caller doesn&#39;t specify any value for parameter &lt;code&gt;b&lt;/code&gt;, then set &lt;code&gt;b = 10&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can call this function in two ways:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;10, 20&rpar;&lt;/code&gt; with this 10 will be assigned to the first parameter i.e. &lt;code&gt;a&lt;/code&gt; and 20 will be assigned to &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;10&rpar;&lt;/code&gt; with this 10 will be assigned to the first parameter i.e. &lt;code&gt;a&lt;/code&gt; and as the user didn&#39;t provide the second argument, python will look at the second parameter and assign it the default value that is present in the function definition.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;f&#39;a=&lt;span class=&quot;hljs-subst&quot;&gt;{a}&lt;/span&gt; and b=&lt;span class=&quot;hljs-subst&quot;&gt;{b}&lt;/span&gt;&#39;&lt;/span&gt;&rpar;

my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT -------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Suppose we have three parameters and we want to make the second parameter optional.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we define a function &lt;code&gt;my_func&lpar;a, b = 100, c&rpar;&lt;/code&gt; with these three parameters.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, how would we call this function without specifying a value for the second parameter?&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we call it like this &lt;code&gt;my_func&lpar;10, 20&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Is this correct?&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;I don&#39;t think so, let&#39;s check.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;10 will be assigned to &lt;code&gt;a&lt;/code&gt; and 20 will be assigned to..., which one &lt;code&gt;b&lt;/code&gt; or &lt;code&gt;c&lt;/code&gt;?&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, python can&#39;t tell which one this value should be assigned to.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In conclusion, if a positional parameter is defined with a default value, then every positional parameter after it must also be given a default value.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;f&#39;a=&lt;span class=&quot;hljs-subst&quot;&gt;{a}&lt;/span&gt; and b=&lt;span class=&quot;hljs-subst&quot;&gt;{b}&lt;/span&gt; and c=&lt;span class=&quot;hljs-subst&quot;&gt;{c}&lt;/span&gt;&#39;&lt;/span&gt;&rpar;

my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT ------------- #&lt;/span&gt;
    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, c&lt;/span&gt;&rpar;:&lt;/span&gt;
                          ^
SyntaxError: non-default argument follows default argument
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;So, in the above example, we have to put a default value for &lt;code&gt;c&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we defined a function &lt;code&gt;my_func&lpar;a, b=2, c=3&rpar;&lt;/code&gt; with these parameters.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, all the following calls are possible:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1&rpar;&lt;/code&gt;, here 1 will be assigned to &lt;code&gt;a&lt;/code&gt;, and for &lt;code&gt;b&lt;/code&gt; and &lt;code&gt;c&lt;/code&gt; the respective default values will be assigned.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1,20&rpar;&lt;/code&gt;, here 1 will be assigned to &lt;code&gt;a&lt;/code&gt;, 20 will be assigned to &lt;code&gt;b&lt;/code&gt; and for &lt;code&gt;c&lt;/code&gt;, the default value will be assigned.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1,20,30&rpar;&lt;/code&gt;, here 1 will be assigned to &lt;code&gt;a&lt;/code&gt;, 20 will be assigned to &lt;code&gt;b&lt;/code&gt; and 30 will be assigned to &lt;code&gt;c&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}, c={2}&quot;&lt;/span&gt;.format&lpar;a, b, c&rpar;&rpar;

my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------- OUTPUT ---------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;But let&#39;s say we want to specify the first and the third parameter arguments and take the default value for the second parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, how can we do this?&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, we need the help of keyword arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-keyword-arguments&quot;&gt;Keyword Arguments&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;To accomplish the above task, you can do this:&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;a=30, c=10&rpar;&lt;/code&gt;, by calling this way, you are saying that you want the value for &lt;code&gt;a&lt;/code&gt; to be 30 and the value for &lt;code&gt;c&lt;/code&gt; to be 10.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Positional arguments, can &lt;strong&gt;optionally&lt;/strong&gt;, be specified using their corresponding parameter name.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This allows us to pass the arguments without sticking to the order of parameters.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, the argument names must be the same as the parameter names.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The following calls are possible:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;a=30, c=10&rpar;&lt;/code&gt;, by calling this way, you are saying that you want the value for &lt;code&gt;a&lt;/code&gt; to be 30 and the value for &lt;code&gt;c&lt;/code&gt; to be 10.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;10, c=30&rpar;&lt;/code&gt;, by calling this way, you are saying that you want the value for &lt;code&gt;a&lt;/code&gt; to be 10, the value for &lt;code&gt;b&lt;/code&gt; should be the default value and the value for &lt;code&gt;c&lt;/code&gt; should be 30.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_func&lpar;a=&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------- OUTPUT --------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;We can also use keyword arguments even if the function parameter doesn&#39;t have any default values.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we define a function &lt;code&gt;my_func&lpar;a, b, c&rpar;&lt;/code&gt;, notice none of the parameters have a default value.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can call the above function in multiple ways:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1, 2, 3&rpar;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1, 2, c=3&rpar;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;a=1, b=2, c=3&rpar;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;b=2, a=1, c=3&rpar;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;f&#39;a=&lt;span class=&quot;hljs-subst&quot;&gt;{a}&lt;/span&gt; and b=&lt;span class=&quot;hljs-subst&quot;&gt;{b}&lt;/span&gt; and c=&lt;span class=&quot;hljs-subst&quot;&gt;{c}&lt;/span&gt;&#39;&lt;/span&gt;&rpar;

my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
my_func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
my_func&lpar;a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
my_func&lpar;b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT ---------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In conclusion, by using keyword arguments, you don&#39;t need to stick to the order of parameters, you can write them in whichever way you want.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, once you use a named argument, all arguments thereafter must be named too.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say you call the above-defined function like this:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;code&gt;my_func&lpar;c=1, 2, 4&rpar;&lt;/code&gt;, now Python looks at this and it&#39;s like okay, 1 is assigned to &lt;code&gt;c&lt;/code&gt;, but then what, python can&#39;t determine which value is for which parameter.&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Lastly, using keyword arguments and default arguments, the following calls are possible:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;1&rpar;&lt;/code&gt;, here 1 will be assigned to &lt;code&gt;a&lt;/code&gt;, &lt;code&gt;b&lt;/code&gt; and &lt;code&gt;c&lt;/code&gt; will be assigned to their respective default values.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;a=1, b=2&rpar;&lt;/code&gt;, here 1 will be assigned to &lt;code&gt;a&lt;/code&gt;, 2 will be assigned to &lt;code&gt;b&lt;/code&gt; and c will get its default value.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_func&lpar;c=3, a=1&rpar;&lt;/code&gt;, here 3 will be assigned to &lt;code&gt;c&lt;/code&gt;, 1 will be assigned to &lt;code&gt;a&lt;/code&gt; and b will get its default value.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-unpacking-iterables&quot;&gt;Unpacking Iterables&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;What defines a tuple in Python, it&#39;s not &lt;code&gt;&lpar;&rpar;&lt;/code&gt;, instead, it&#39;s &lt;code&gt;,&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;&lpar;&rpar;&lt;/code&gt; is used to make it look clearer.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;1,2,3&lt;/code&gt; is also a tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;To create a tuple with a single element, you can do &lt;code&gt;1,&lt;/code&gt; or &lt;code&gt;&lpar;1,&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;To create an empty tuple, you can do &lt;code&gt;tuple&lpar;&rpar;&lt;/code&gt; or &lt;code&gt;&lpar;&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------- #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;,&rpar;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------- OUTPUT ------------ #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;,
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT -------------- #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;It won&#39;t be a tuple if you removed the &lt;code&gt;,&lt;/code&gt;.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;&rpar;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT ------------- #&lt;/span&gt;
int
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;To create an empty tuple, there are two ways:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lpar;&rpar;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT ------------ #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = tuple&lpar;&rpar;
type&lpar;a&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT ------------- #&lt;/span&gt;
tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Packed values refer to values that are bundled together in some way.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Tuples and lists are obvious.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Strings are considered packed values because characters are bundled together.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Sets and dictionaries are also packed values.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;A dictionary is a collection of key-value pairs.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Any iterable can be considered a packed value.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-unpacking-packed-values&quot;&gt;Unpacking packed values&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Unpacking is the act of splitting packed values into individual variables contained in a list or tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In other words, you create a tuple or a list that contains variable names and then you unpack the iterable into the variable names.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say you have a list &lt;code&gt;[1, 2, 3]&lt;/code&gt; and you want to unpack the list into a tuple &lt;code&gt;a, b, c&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, there are 3 variables in the list, so we need 3 variables to unpack.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, the result will be:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a&lt;/code&gt; will be 1&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;b&lt;/code&gt; will be 2&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;c&lt;/code&gt; will be 3&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;l = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;]
a, b, c, d = l
print&lpar;a, b, c, d&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT -------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Unpacking into individual variables is based on the relative positions of each element.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Unpacking other iterables:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, c = 10, 20, &#39;hello&#39;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, c = &#39;XYZ&#39;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, b, c = &lt;span class=&quot;hljs-string&quot;&gt;&#39;XYZ&#39;&lt;/span&gt;
print&lpar;a, b, c&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------- OUTPUT ------------- #&lt;/span&gt;
X Y Z
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;You can use this while swapping two values.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# traditional way for swapping two variables&lt;/span&gt;
a = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
b = &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}&quot;&lt;/span&gt;.format&lpar;a, b&rpar;&rpar;

tmp = a
a = b
b = tmp
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}&quot;&lt;/span&gt;.format&lpar;a, b&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------- OUTPUT -------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# using unpacking&lt;/span&gt;
a = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
b = &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}&quot;&lt;/span&gt;.format&lpar;a, b&rpar;&rpar;

a, b = b, a
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a={0}, b={1}&quot;&lt;/span&gt;.format&lpar;a, b&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------- OUTPUT --------------- #&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
a=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;While unpacking dictionaries:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;let&#39;s say we have a dictionary &lt;code&gt;d = {&#39;key1&#39;: 1, &#39;key2&#39;: 2, &#39;key3&#39;: 3}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, if we write &lt;code&gt;a, b, c = d&lt;/code&gt;, we will get the keys of the dictionary and not the values.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;dict1 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;p&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;}
dict1
a, b, c, d, e, f = dict1
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;
print&lpar;e&rpar;
print&lpar;f&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
p
y
t
h
o
n
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Note: Python Dictionary is ordered after Python 3.6 but sets are still unordered.&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a&lt;/code&gt; will be &lt;code&gt;key1&lt;/code&gt;, &lt;code&gt;b&lt;/code&gt; will be &lt;code&gt;key2&lt;/code&gt; and &lt;code&gt;c&lt;/code&gt; will be &lt;code&gt;key3&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;While using sets:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;let&#39;s say we have a set &lt;code&gt;s = {&#39;h&#39;, &#39;e&#39;, &#39;l&#39;, &#39;l&#39;, &#39;o&#39;}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;If we unpack we can get different answers this is also an unordered type.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;s = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;p&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;}
print&lpar;s&rpar;
a, b, c, d, e, f = s

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;p&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;}
p
t
y
n
o
h
&lt;/code&gt;&lt;/pre&gt;
&lt;h2 id=&quot;heading-extended-unpacking-and&quot;&gt;Extended Unpacking&lpar;* and ** &rpar;&lt;/h2&gt;
&lt;h3 id=&quot;heading-use-case-for&quot;&gt;Use case for *&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;We always don&#39;t want to unpack every single element in an iterable.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We may, for example, want to unpack the first value, and then unpack the remaining values into another variable.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have a list &lt;code&gt;l = [1, 2, 3, 4, 5, 6]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can achieve our goal in multiple ways:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Using slicing:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;You can do &lt;code&gt;a = l[0]&lt;/code&gt; and &lt;code&gt;b = l[1:]&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Using simple unpacking:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;code&gt;a, b = l[0], l[1:]&lt;/code&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Using * operator:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;code&gt;a, *b = l&lt;/code&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;l = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;]
&lt;span class=&quot;hljs-comment&quot;&gt;# using slicing&lt;/span&gt;
a = l[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;]
b = l[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;:]
print&lpar;a&rpar;
print&lpar;b&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT -------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# using unpacking &lt;/span&gt;
a, b = l[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;], l[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;:]
print&lpar;a&rpar;
print&lpar;b&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# using * operator&lt;/span&gt;
a, *b = l
print&lpar;a&rpar;
print&lpar;b&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Let&#39;s see another example with tuples&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, *b = &lt;span class=&quot;hljs-number&quot;&gt;-10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;
print&lpar;a&rpar;
print&lpar;b&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;-10&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Let&#39;s take another example with strings&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, *b = &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;
print&lpar;a&rpar;
print&lpar;b&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
p
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;What about extracting the first, second, last and the rest elements?&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# with slicing&lt;/span&gt;
s = &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;

a, b, c, d = s[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;], s[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;], s[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;:&lt;span class=&quot;hljs-number&quot;&gt;-1&lt;/span&gt;], s[&lt;span class=&quot;hljs-number&quot;&gt;-1&lt;/span&gt;]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT ------------ #&lt;/span&gt;
p
y
tho
n
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# with unpacking&lt;/span&gt;
a, b, *c, d = s
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
p
y
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;]
n
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;c&lt;/code&gt; is a list of characters and not a string, if that&#39;s a problem then you can use the &lt;code&gt;join&lpar;&rpar;&lt;/code&gt; function to get the string from list.&lt;/p&gt;
&lt;h4 id=&quot;heading-usage-with-ordered-types&quot;&gt;Usage with Ordered Types&lt;/h4&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b = [1, 2, 3, 4]&lt;/code&gt;, then &lt;code&gt;a = 1&lt;/code&gt; and &lt;code&gt;b = [2, 3, 4]&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b = &lpar;10, 20, 30, 40&rpar;&lt;/code&gt;, then &lt;code&gt;a = 10&lt;/code&gt; and &lt;code&gt;b = [20, 30, 40]&lt;/code&gt; &lpar;notice we always get a list type after unpacking&rpar;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b = &#39;XYZ&#39;&lt;/code&gt;, then &lt;code&gt;a = &#39;X&#39;&lt;/code&gt; and &lt;code&gt;b = [&#39;Y&#39;, &#39;Z&#39;]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, *c = 1, 2, 3, 4, 5&lt;/code&gt;, then &lt;code&gt;a = 1&lt;/code&gt;, &lt;code&gt;b = 2&lt;/code&gt;, and &lt;code&gt;c = [3, 4, 5]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, *c, d = 1, 2, 3, 4, 5, 6&lt;/code&gt;, then &lt;code&gt;a = 1&lt;/code&gt;, &lt;code&gt;b = 2&lt;/code&gt;, &lt;code&gt;c = [3, 4]&lt;/code&gt;, and &lt;code&gt;d = 5&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b, c, d = &#39;python&#39;&lt;/code&gt;, then &lt;code&gt;a = &#39;p&#39;&lt;/code&gt;, &lt;code&gt;b = [&#39;y&#39;, &#39;t&#39;, &#39;h&#39;]&lt;/code&gt;, &lt;code&gt;c = &#39;o&#39;&lt;/code&gt; and &lt;code&gt;d = &#39;n&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b = {&#39;p&#39;:1, &#39;y&#39;: 2, &#39;t&#39;: 3, &#39;h&#39;: 4, &#39;o&#39;: 5, &#39;n&#39;: 6}&lt;/code&gt;, then &lt;code&gt;a=&#39;p&#39;&lt;/code&gt; and &lt;code&gt;b = [&#39;y&#39;, &#39;t&#39;, &#39;h&#39;, &#39;o&#39;, &#39;n&#39;]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can&#39;t get key-value pairs by unpacking from RHS, but we can get key-value pairs while unpacking from LHS.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Till now, we have seen that we can unpack from RHS, but we can also unpack from LHS.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have &lt;code&gt;l1 = [1, 2, 3]&lt;/code&gt; and &lt;code&gt;l2 = [4, 5, 6]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then to unpack this we can write &lt;code&gt;l = [*l1, *l2]&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This will result in &lt;code&gt;l = [1,2,3,4,5,6]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you can see this unpacks the two lists into individual elements.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s take another example with dictionaries.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;d1 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
d2 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}
[*d1, *d2]

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT --------- #&lt;/span&gt;
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;But how can we unpack both key and value?&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;d1 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
d2 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}

{**d1, **d2}

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ---------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Notice that the value for key &lt;code&gt;key2&lt;/code&gt; is 3 and not 2, but why?&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;It&#39;s because the dictionary &lt;code&gt;d2&lt;/code&gt; is merged last, so it overwrote the value for key &lt;code&gt;key2&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h4 id=&quot;heading-usage-with-unordered-types&quot;&gt;Usage with Unordered Types&lt;/h4&gt;
&lt;p&gt;You can use the * operator in unordered types, but the problem is you will never know what&#39;s the first element, what&#39;s the second element and so on.&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;But this is useful when you want to unpack in the RHS.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have 3 dictionaries:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d1 = {&#39;p&#39;: 1, &#39;y&#39;: 2}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d2 = {&#39;t&#39;: 3, &#39;h&#39;: 4}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d3 = {&#39;h&#39;: 5, &#39;o&#39;: 6, &#39;n&#39;: 7}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we want to get all the unique keys, then what we can do is we can unpack all the keys of these dictionaries into a set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, &lt;code&gt;s = {*d1, *d2, *d2}&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This will result in &lt;code&gt;s = {&#39;p&#39;, &#39;y&#39;, &#39;t&#39;, &#39;h&#39;, &#39;o&#39;, &#39;n&#39;}&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-use-case-for-1&quot;&gt;Use case for **&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;You can&#39;t use the ** operator on the LHS, you can only use it on RHS.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have 3 dictionaries:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d1 = {&#39;p&#39;: 1, &#39;y&#39;: 2}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d2 = {&#39;t&#39;: 3, &#39;h&#39;: 4}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d3 = {&#39;h&#39;: 5, &#39;o&#39;: 6, &#39;n&#39;: 7}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d = {**d1, **d2, **d3}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d = {&#39;p&#39;: 1, &#39;y&#39;: 2, &#39;t&#39;: 3, &#39;h&#39;: 5, &#39;o&#39;: 6, &#39;n&#39;: 7}&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you may have noticed, the value of &lt;code&gt;h&lt;/code&gt; in &lt;code&gt;d&lt;/code&gt; is 5 even though there are two different values for the key &lt;code&gt;h&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The resulting dictionary took the value &lt;code&gt;5&lt;/code&gt; because &lt;code&gt;d3&lt;/code&gt; is mergerd at the end and it overwrote the value for the key &lt;code&gt;h&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You can even use it to add key-value pairs from one or more dictionaries into a dictionary literal.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have a dictionary &lt;code&gt;d1 = {&#39;a&#39;: 1, &#39;b&#39;: 2}&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we create another dictionary and we want to add/merge the &lt;code&gt;d1&lt;/code&gt; dictionary into this dictionary, then to do this:&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d2 = {&#39;a&#39;: 10, &#39;c&#39;: 3, **d1}&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This will result in &lt;code&gt;d2 = {&#39;a&#39;: 1, &#39;b&#39;: 2, &#39;c&#39;: 3}&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You may ask why the value of &lt;code&gt;a&lt;/code&gt; is 1.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The reason is &lt;code&gt;d1&lt;/code&gt; is merged at the end so it overwrote the value of &lt;code&gt;a&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;d1 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
d2 = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}

{**d1, **d2}

&lt;span class=&quot;hljs-comment&quot;&gt;# --------- OUTPUT ---------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;{**d2, **d1}

&lt;span class=&quot;hljs-comment&quot;&gt;# --------- OUTPUT ----------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, you can see that the value for &lt;code&gt;key2&lt;/code&gt; is 2 as &lt;code&gt;d1&lt;/code&gt; is merged at the end.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;{&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, **d1, **d2, &lt;span class=&quot;hljs-string&quot;&gt;&#39;c&#39;&lt;/span&gt;:&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;c&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, **d1, **d2, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key3&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;h3 id=&quot;heading-nested-unpacking&quot;&gt;Nested Unpacking&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Python supports nested unpacking as well.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have a nested list &lt;code&gt;l = [1, 2, [3, 4]]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can unpack this in multiple ways:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, c = l&lt;/code&gt;, this will result in &lt;code&gt;a = 1&lt;/code&gt;, &lt;code&gt;b = 2&lt;/code&gt;, and &lt;code&gt;c = [3, 4]&lt;/code&gt; and then we&#39;ll have to unpack &lt;code&gt;c&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, b, &lpar;c, d&rpar; = l&lt;/code&gt;, this will reslult in &lt;code&gt;a = 1&lt;/code&gt;, &lt;code&gt;b = 2&lt;/code&gt;, &lt;code&gt;c = 3&lt;/code&gt;, &lt;code&gt;d = 4&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The above method will work with string as well.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;a, *b, &lpar;c, *d&rpar; = [1, 2, 3, &#39;python&#39;]&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This will result in &lt;code&gt;a = 1&lt;/code&gt;, &lt;code&gt;b = [2, 3]&lt;/code&gt;, &lt;code&gt;c = &#39;p&#39;&lt;/code&gt;, and &lt;code&gt;d = [&#39;y ,&#39;t&#39; ,&#39;h&#39; ,&#39;o&#39; ,&#39;n&#39;]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, b, &lpar;c, d&rpar; = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, [&lt;span class=&quot;hljs-string&quot;&gt;&#39;X&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;Y&#39;&lt;/span&gt;]]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT --------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
X
Y
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, b, &lpar;c, d&rpar; = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;XY&#39;&lt;/span&gt;]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
X
Y
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, b, &lpar;c, d, *e&rpar; = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;
print&lpar;e&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
p
y
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, *b, &lpar;c, d, *e&rpar; = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;c&rpar;
print&lpar;d&rpar;
print&lpar;e&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
p
y
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, *b, tmp = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;]
print&lpar;a&rpar;
print&lpar;b&rpar;
print&lpar;tmp&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# --------- OUTPUT --------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
python
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;c, d, *e = tmp
print&lpar;c&rpar;
print&lpar;d&rpar;
print&lpar;e&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
p
y
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;t&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;h&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;o&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;n&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;h2 id=&quot;heading-args&quot;&gt;Args&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In Python, the &lt;code&gt;*args&lt;/code&gt; concept is used to pass a variable number of arguments to a function. The &lt;code&gt;*args&lt;/code&gt; parameter allows you to pass any number of positional arguments to a function, and it collects them into a tuple within the function. The asterisk &lpar;*&rpar; before &lt;code&gt;args&lt;/code&gt; is what enables this behavior.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now let&#39;s see how we can use *args in function parameters.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Recall that in unpacking, &lt;code&gt;a, b, *c = 10, 20, &#39;a&#39;, &#39;b&#39;&lt;/code&gt; will result in &lt;code&gt;a = 10&lt;/code&gt;, &lt;code&gt;b = 20&lt;/code&gt; and &lt;code&gt;c = [&#39;a&#39;, &#39;b&#39;]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a, b, *c = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;

print&lpar;a, b&rpar;
print&lpar;c&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
[&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;A similar thing happens with function parameters.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *args&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a&rpar;
    print&lpar;b&rpar;
    print&lpar;args&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In functions, args will be a tuple and not a list&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The &lt;code&gt;*args&lt;/code&gt; syntax allows flexibility since you don&#39;t have to specify the exact number of arguments in advance. You can pass any number of arguments to the function, including none at all.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The name of parameter args is a convention, you can use any name you want.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *my_vars&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a&rpar;
    print&lpar;b&rpar;
    print&lpar;my_vars&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;c&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;c&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;You can&#39;t use any positional arguments after the args parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;When you call a function with some arguments, the arguments get unpacked in multiple variables which are the parameters of the function.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# unpacking an iterable into positional arguments&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a&rpar;
    print&lpar;b&rpar;
    print&lpar;c&rpar;

l = [&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;]
func1&lpar;*l&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Conventionally, we call it *args.&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-args-with-keyword-arguments&quot;&gt;Args with keyword Arguments&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;Let&#39;s recall positional arguments.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a = 10&lt;/code&gt;, &lt;code&gt;b = 20&lt;/code&gt; and &lt;code&gt;c = 30&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, positional parameters defined in the function can also be passed as named/keyword arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func1&lpar;b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------- OUTPUT --------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;We can make users use keyword arguments by exhausting all positional arguments using &lt;code&gt;*args&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *args, d&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, args, d&rpar;


func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt; &lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;&rpar; &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, you can see the variables &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; gets assigned to the first and second arguments respectively, the args get assigned to the next two string arguments and finally the keyword argument &lt;code&gt;d&lt;/code&gt; gets assigned to the value &lt;code&gt;100&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You can also use args when you don&#39;t want mandatory positional arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# optional positional arguments and mandatory keyword arguments&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*args, d&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;args&rpar;
    print&lpar;d&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT --------- #&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
hello
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func1&lpar;d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
&lpar;&rpar;
hello
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Let&#39;s say you want a function that will only accept keyword arguments and no positional arguments.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;d&rpar;

func1&lpar;d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;bye&#39;&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
bye
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In this function definition, the * operator is used before the parameter list, indicating that all subsequent parameters should be keyword-only arguments. In other words, these parameters can only be passed using their corresponding keywords.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s take another example, which takes no positional arguments and 2 keyword arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# two keyword arguments are compulsory&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, a, b&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a&rpar;
    print&lpar;b&rpar;

func1&lpar;a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Unlike positional parameters, keyword arguments do not have to be defined with non-defaulted and then defaulted arguments&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, *, b=&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, c=&lt;span class=&quot;hljs-string&quot;&gt;&#39;bye&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt; hello bye
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a = 5&lt;/code&gt;, then &lt;code&gt;*&lt;/code&gt; denotes no positional argument after this only keyword arguments will be allowed, then &lt;code&gt;c = &#39;bye&#39;&lt;/code&gt;, &lt;code&gt;b = &#39;hello&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s see some examples.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func1&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;, *args, d=&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;, e=&lt;span class=&quot;hljs-string&quot;&gt;&#39;n/a&#39;&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, args, d, e&rpar;

func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;, e=&lt;span class=&quot;hljs-string&quot;&gt;&#39;all engines running&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt; &lpar;&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;&rpar; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt; all engines running
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a = 5&lt;/code&gt;, &lt;code&gt;b = 4&lt;/code&gt;, &lt;code&gt;args = &lpar;3, 2, 1&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;After this only keyword arguments are there and there are 2 keyword arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d = 0&lt;/code&gt; and &lt;code&gt;e = &#39;all engines running&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;600&lt;/span&gt;, d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;goooood morning&#39;&lt;/span&gt;, e=&lt;span class=&quot;hljs-string&quot;&gt;&#39;python!&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;600&lt;/span&gt; &lpar;&rpar; goooood morning python!
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a = 0&lt;/code&gt;, &lt;code&gt;b = 600&lt;/code&gt;, and as there are no more positional arguments so &lt;code&gt;args = &lpar;&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d = goooood morning&lt;/code&gt; and &lt;code&gt;e = &#39;python!&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func1&lpar;&lt;span class=&quot;hljs-number&quot;&gt;11&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;m/s&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;24&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;mph&#39;&lt;/span&gt;, d=&lt;span class=&quot;hljs-string&quot;&gt;&#39;unladen&#39;&lt;/span&gt;, e=&lt;span class=&quot;hljs-string&quot;&gt;&#39;swallow&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------- OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;11&lt;/span&gt; m/s &lpar;&lt;span class=&quot;hljs-number&quot;&gt;24&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;mph&#39;&lt;/span&gt;&rpar; unladen swallow
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a = 11&lt;/code&gt;, &lt;code&gt;b = &#39;m/s&#39;&lt;/code&gt;, &lt;code&gt;args = &lpar;24, &#39;mph&#39;&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;d = &#39;unladen&#39;&lt;/code&gt; and &lt;code&gt;e = &#39;swallow&#39;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-kwargs&quot;&gt;kwargs&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;*args is used to scoop up a variable amount of remaining positional arguments and it returns a tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here the parameter name args is arbitrary, the real parameter here is *.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;**kwargs is used to scoop up a variable amount of remaining keyword arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;It&#39;ll return a dictionary&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;**kwargs can be specified even if the positional arguments have not been exhausted.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s see some examples&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;**kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;kwargs&rpar;

func&lpar;x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;We can also use it in conjunction with &lt;strong&gt;*args&lt;/strong&gt;:&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*args, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;args&rpar;
    print&lpar;kwargs&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;&rpar;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;a&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;b&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Note: You cannot do the following:&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;kwargs&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;There is no need to even do this, since &lt;strong&gt;**kwargs&lt;/strong&gt; essentially indicates no more positional arguments.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a&rpar;
    print&lpar;b&rpar;
    print&lpar;kwargs&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Also, you cannot specify parameters &lt;strong&gt;after&lt;/strong&gt; &lt;strong&gt;**kwargs&lt;/strong&gt; has been used:&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, **kwargs, c&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;pass&lt;/span&gt;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, **kwargs, c&lt;/span&gt;&rpar;:&lt;/span&gt;
                             ^
SyntaxError: invalid syntax
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;If you want to specify both specific keyword-only arguments and &lt;strong&gt;**kwargs&lt;/strong&gt; you will need to first get to a point where you can define a keyword-only argument &lpar;i.e. exhaust the positional arguments, using either &lt;strong&gt;*args&lt;/strong&gt; or just &lt;strong&gt;*&lt;/strong&gt;&rpar;&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, d, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;d&rpar;
    print&lpar;kwargs&rpar;

func&lpar;d=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;h2 id=&quot;heading-putting-it-all-together&quot;&gt;Putting It All Together&lt;/h2&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;#positionals only&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b&rpar;

func&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;world&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT --------- #&lt;/span&gt;
hello world
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;b=&lt;span class=&quot;hljs-string&quot;&gt;&#39;world&#39;&lt;/span&gt;, a=&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ------------ #&lt;/span&gt;
hello world
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;#positionals only: no extra positionals, only defaults&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-string&quot;&gt;&#39;world&#39;&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c&rpar;

func&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ------------ #&lt;/span&gt;
hello world &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;, c=&lt;span class=&quot;hljs-string&quot;&gt;&#39;!&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
hello world !
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# positionals only: extra positionals, no defaults&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *args&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, args&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords only: no positionals, no defaults&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, a, b&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b&rpar;

func&lpar;a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords only: no positionals, some defaults&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*, a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b&rpar;

func&lpar;a=&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords and positionals: some positionals&lpar;no defaults&rpar;, keywords&lpar;no defaults&rpar;&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *, c, d&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c, d&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords and positionals: some positional defaults&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, *, c, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c, d&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords and positionals: extra positionals&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, *args, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, args, c, d&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;&rpar; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------- OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; x &lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;&rpar; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywrods and positionals: no extra positionals, extra keywords&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *, c, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, c, d, kwargs&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, z=&lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------- OUTPUT ----------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt; {&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;func&lpar;x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, z=&lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, b=&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, a=&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt; {&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# keywords and positionals: extra positionals, extra keywords&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b, *args, c, d=&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;a, b, args, c, d, kwargs&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;, c=&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, d=&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, z=&lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------ OUTPUT ---------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; &lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;&rpar; &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt; &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt; {&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;#keywords and positionals: extra positionals and extra keywords&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;func&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;*args, **kwargs&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;args, kwargs&rpar;

func&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, x=&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, y=&lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, z=&lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------- OUTPUT ------------- #&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar; {&lt;span class=&quot;hljs-string&quot;&gt;&#39;x&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;y&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;200&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;z&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;300&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;h1 id=&quot;heading-conclusion&quot;&gt;Conclusion&lt;/h1&gt;
&lt;p&gt;In conclusion, mastering Python function arguments is essential for writing efficient and clean code. By understanding the differences between parameters and arguments, utilizing positional and keyword arguments, and leveraging unpacking, &lt;em&gt;args, and&lt;/em&gt; *kwargs, you&#39;ll be better equipped to tackle complex programming tasks in Python.&lt;/p&gt;

 <img src="$cover_image" alt="Cover Image" width="200" height="200" align="left">

## [Python Variables Explained: Memory, Mutability, and More](https://neuronize.dev/python-variables-explained-memory-mutability-and-more)

&lt;p&gt;Welcome to my blog post where we will dive into the world of Python variables. If you are new to programming, don&#39;t worry, I have got you covered! In my &lt;a target=&quot;_blank&quot; href=&quot;https://neuronize.dev/quick-python-primer-master-the-basics-in-20-minutes&quot;&gt;previous blog post&lt;/a&gt;, I provided a refresher on the basics of Python programming language. Now, we will move on to the next level and take a closer look at variables in Python. Variables are one of the fundamental concepts in programming and mastering them is essential for writing efficient and effective code. So, let&#39;s get started and explore Python variables in-depth!&lt;/p&gt;
&lt;p&gt;Let&#39;s first take a look at memory.&lt;/p&gt;
&lt;h2 id=&quot;heading-memory&quot;&gt;Memory&lt;/h2&gt;
&lt;p&gt;You can think of memory as a set of blocks where each block has a unique address. Think of it like a real-world example where each house on a street has a unique address. In the same way, each block has a unique address.&lt;/p&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683960631074/4cf799c1-2097-4b60-b4b6-fb19603a5d1d.png&quot; alt=&quot;figure of memory with each block having it&#39;s own unique address&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;Now, let&#39;s dive into variables.&lt;/p&gt;
&lt;h2 id=&quot;heading-variable&quot;&gt;Variable&lt;/h2&gt;
&lt;p&gt;&lt;strong&gt;What happens when you write&lt;/strong&gt; &lt;code&gt;a = 5&lt;/code&gt;?&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Python creates an object in memory in some address, let&#39;s say &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In this object, the value 5 is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683960718378/f8d867c1-ddf1-4d3f-adcc-a8c072d46752.png&quot; alt=&quot;vale 5 is stored in a object at address 0x1000&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, a is you can think of an alias for the memory address &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, &lt;code&gt;a&lt;/code&gt; doesn&#39;t represent the value &lt;code&gt;5&lt;/code&gt; instead it refers to the memory address &lt;code&gt;0x1000&lt;/code&gt; and the address &lt;code&gt;0x1000&lt;/code&gt; refers to the data stored in the object and the data is &lt;code&gt;5&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683960782879/f4c6d7e2-59f0-436a-8aca-ce6486ce3f93.png&quot; alt=&quot;a is referencing to address 0x1000&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;To find out the memory address of the object that the variable is referencing, you can use the &lt;code&gt;id&lpar;&rpar;&lt;/code&gt; function.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# declared a variable a and stored a value 10&lt;/span&gt;
a = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;

&lt;span class=&quot;hljs-comment&quot;&gt;# printing the value, it&#39;s decimal memory address and it&#39;s hex memory address&lt;/span&gt;
print&lpar;a&rpar;
print&lpar;id&lpar;a&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;a&rpar;&rpar;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------------- OUTPUT ------------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;4376986128&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x104e38210&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, I declared a variable &lt;code&gt;a&lt;/code&gt; with a value of 10. Let&#39;s understand what happened under the hood.&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;First, python created an object at some memory address, let&#39;s say &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In that object, python puts the value 10.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, variable &lt;code&gt;a&lt;/code&gt; refers to the memory address &lt;code&gt;0x1000&lt;/code&gt; that holds the object with the value 10. In the above code, I have printed out the value, the decimal format of the address that the variable &lt;code&gt;a&lt;/code&gt; is referring to and the hexadecimal format of the address.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;Let&#39;s take a look at another example.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;s = &lt;span class=&quot;hljs-string&quot;&gt;&quot;hello&quot;&lt;/span&gt;
print&lpar;s&rpar;
print&lpar;id&lpar;s&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;s&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------------------- OUTPUT --------------------- #&lt;/span&gt;
hello
&lt;span class=&quot;hljs-number&quot;&gt;4702080944&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x118440fb0&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;First, python created an object at some memory address with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, the variable &lt;code&gt;s&lt;/code&gt; refers to the memory address that holds the object with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt;. In the above code, I have printed out the value, the decimal format of the address that the variable &lt;code&gt;a&lt;/code&gt; is referring to and the hexadecimal format of the address.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-reference-counting&quot;&gt;Reference Counting&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;So, we just learned how the variables are referencing a memory address where an object is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We can count how many variables are pointing to that same memory address.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we declared a variable &lt;code&gt;a = 5&lt;/code&gt; and let&#39;s say the memory address where the object gets created is &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then the reference count to that memory address is 1.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963033848/b4719fc6-f957-42f5-9386-9cdcd383ed36.png&quot; alt=&quot;reference count goes to 1&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we declared another variable &lt;code&gt;b = a&lt;/code&gt;, where &lt;code&gt;b&lt;/code&gt; is not getting assigned to a value &lt;code&gt;5&lt;/code&gt; instead &lt;code&gt;b&lt;/code&gt; is referencing the variable &lt;code&gt;a&lt;/code&gt; which in turn references the memory location &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Hence, two variables are pointing to the memory address &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, the reference count of the memory address &lt;code&gt;0x1000&lt;/code&gt; is 2.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963120701/79ca5535-4af7-4573-a541-3b4b699fc035.png&quot; alt=&quot;reference count goes to 2&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;Let&#39;s say b got removed either &lt;code&gt;b&lt;/code&gt; is out-of-scope or maybe gets assigned to a different memory location, then the reference count goes to 1.&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963613430/499bb03d-e59e-4c60-b2a6-74424710229b.png&quot; alt=&quot;b got out of scope and reference count goes to 1&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;Let&#39;s say &lt;code&gt;a&lt;/code&gt; also got removed in one of the above ways, then the reference count goes to 0.&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963653254/0c050724-c32c-4b99-88b0-d4b1b73d9c7a.png&quot; alt=&quot;reference count goes to 0&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;At this point, the Python memory manager recognizes this and throws away the object that was there in that memory location.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, the space is freed.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963699406/e519b156-6fe8-45a0-8f53-5ad35ed26ff7.png&quot; alt class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;sys&lt;/code&gt; module has a &lt;code&gt;getrefcount&lpar;&rpar;&lt;/code&gt; function that can be used to get the reference count.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This takes one parameter the variables, but the downside is that it also adds one reference count to that object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;There&#39;s also another way using &lt;code&gt;ctypes&lt;/code&gt; module.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-getrefcount&quot;&gt;getrefcount&lpar;&rpar;&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; sys

&lt;span class=&quot;hljs-comment&quot;&gt;# delcared a list with respective values, print it&#39;s id and then get the reference count&lt;/span&gt;
lst_1 = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
print&lpar;id&lpar;lst_1&rpar;&rpar;
sys.getrefcount&lpar;lst_1&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------------- OUTPUT --------------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;4389242752&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;It says 2 as the method &lt;code&gt;getrefcount&lpar;&rpar;&lt;/code&gt; is also referencing the address, so the reference count increases, to get the actual reference count, just subtract 1 from the answer.&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-ctypes&quot;&gt;ctypes&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# with `ctypes`, you can get the actual reference count as it takes the actual memory address and not the reference.&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; ctypes

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;ref_count&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;address&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; ctypes.c_long.from_address&lpar;address&rpar;.value

&lt;span class=&quot;hljs-comment&quot;&gt;# here you can see you get 1 as the reference count which is correct&lt;/span&gt;
print&lpar;id&lpar;lst_1&rpar;&rpar;
ref_count&lpar;id&lpar;lst_1&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------------- OUTPUT ------------------ #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;4389242752&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;h2 id=&quot;heading-garbage-collection&quot;&gt;Garbage Collection&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Previously, we learned that as soon as the reference count goes to 0, the Python memory manager destroys the object that&#39;s in the memory location and free&#39;s up the memory location.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;But this doesn&#39;t work always and one of the cases where this doesn&#39;t work is circular references.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s think of a scenario where variable &lt;code&gt;a&lt;/code&gt; is referencing the variable &lt;code&gt;b&lt;/code&gt; and variable &lt;code&gt;b&lt;/code&gt; is referencing the variable &lt;code&gt;c&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963750338/e662de45-30e2-4efb-ba0d-5580a525aff1.png&quot; alt=&quot;a is referencing to b and b is referencing to c&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Now, let&#39;s say we delete the variable &lt;code&gt;a&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;  &lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963825263/3b146713-d8a7-4386-9f65-053c9cb2d6b8.png&quot; alt=&quot;reference count of 0x1002 is 0&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, the reference count of &lt;code&gt;b&lt;/code&gt; is 0 but the reference count of &lt;code&gt;c&lt;/code&gt; is 1.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, the second object will be destroyed, then the reference count of the third object will become 0 and it&#39;ll get destroyed too.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, let&#39;s say the variable &lt;code&gt;c&lt;/code&gt; is also referencing the variable &lt;code&gt;b&lt;/code&gt;. i.e &lt;code&gt;c = b&lt;/code&gt; and after that, we removed variable &lt;code&gt;a&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963905326/f44e0085-bd97-4f15-aa11-d5b79c1711e8.png&quot; alt=&quot;circular reference between b and c&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Now, both object has reference count = 1.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, none of the objects are going to get destroyed as both have a reference count of 1 and this scenario is known as circular referencing.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As python memory manager can&#39;t eliminate these objects and if we continue like this, this will result in a memory leak.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, the Garbage collector comes to the rescue, it can handle this kind of issue.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You can control the garbage collector programmatically using &lt;code&gt;gc&lt;/code&gt; module.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You can call it manually and even do your cleanup.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; gc
&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; ctypes

&lt;span class=&quot;hljs-comment&quot;&gt;# function to count the references&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;ref_count&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;address&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; ctypes.c_long.from_address&lpar;address&rpar;.value
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;I imported the gc and ctypes modules and defined the reference count function to count the reference count.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# this function will return if the given object_id is in the garbage collector or not&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;object_by_id&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;object_id&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; obj &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; gc.get_objects&lpar;&rpar;:
        &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; id&lpar;obj&rpar; == object_id:
            &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;hljs-string&quot;&gt;&quot;Object exists&quot;&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;hljs-string&quot;&gt;&quot;Not found&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;This function will take the id of an object as an argument and then it&#39;ll return &quot;Object exists&quot; if the garbage collector has tracked that this object is in some circular reference else it&#39;ll return &quot;Not found&quot; i.e. the given object is not in any circular reference.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# created two classes to illustrate the circular reference concept&lt;/span&gt;
&lt;span class=&quot;hljs-class&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;A&lt;/span&gt;:&lt;/span&gt;
    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;__init__&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;self&lt;/span&gt;&rpar;:&lt;/span&gt;
        self.b = B&lpar;self&rpar;
        print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;A: self: {0}, b:{1}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;self&rpar;&rpar;, hex&lpar;id&lpar;self.b&rpar;&rpar;&rpar;&rpar;


&lt;span class=&quot;hljs-class&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;B&lt;/span&gt;:&lt;/span&gt;
    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;__init__&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;self, a&lt;/span&gt;&rpar;:&lt;/span&gt;
        self.a = a
        print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;B: self: {0}, a: {1}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;self&rpar;&rpar;, hex&lpar;id&lpar;self.a&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Now, I created two classes A and B to illustrate the circular reference.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;class A&lt;/code&gt;: - This line defines a new class called A.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;def __init__&lpar;self&rpar;&lt;/code&gt;: - This is the constructor of the A class. It is executed when a new instance of the class is created.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;self.b = B&lpar;self&rpar;&lt;/code&gt; - This line creates a new instance of the B class and assigns it to the b attribute of the current instance of the A class. The self-argument passed to the B constructor is a reference to the current instance of the A class.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;print&lpar;&#39;A: self: {0}, b:{1}&#39;.format&lpar;hex&lpar;id&lpar;self&rpar;&rpar;, hex&lpar;id&lpar;self.b&rpar;&rpar;&rpar;&rpar;&lt;/code&gt; - This line prints a message to the console. The message contains the hexadecimal representations of the memory addresses of the current instance of the A class and its b attribute.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;class B&lt;/code&gt;: - This line defines a new class called B.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;def __init__&lpar;self, a&rpar;&lt;/code&gt;: - This is the constructor of the B class. It is executed when a new instance of the class is created. The &lt;code&gt;a&lt;/code&gt; argument is a reference to an instance of the A class.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;self.a&lt;/code&gt; = a - This line assigns the &lt;code&gt;a&lt;/code&gt; argument to the &lt;code&gt;a&lt;/code&gt; attribute of the current instance of the B class.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;print&lpar;&#39;B: self: {0}, a: {1}&#39;.format&lpar;hex&lpar;id&lpar;self&rpar;&rpar;, hex&lpar;id&lpar;self.a&rpar;&rpar;&rpar;&rpar;&lt;/code&gt; - This line prints a message to the console. The message contains the hexadecimal representations of the memory addresses of the current instance of the B class and its &lt;code&gt;a&lt;/code&gt; attribute.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# We disabled the garbage collector, so that we can run it manually and also check the reference count.&lt;/span&gt;
gc.disable&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Now, we disabled the garbage collector, so that we can run it manually.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# create an instance of class A&lt;/span&gt;
my_var = A&lpar;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT --------------- #&lt;/span&gt;
B: self: &lt;span class=&quot;hljs-number&quot;&gt;0x11953e8c0&lt;/span&gt;, a: &lt;span class=&quot;hljs-number&quot;&gt;0x11953d8d0&lt;/span&gt;
A: self: &lt;span class=&quot;hljs-number&quot;&gt;0x11953d8d0&lt;/span&gt;, b:&lt;span class=&quot;hljs-number&quot;&gt;0x11953e8c0&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;I created an instance of A.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This prints out the ids of &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The id of &lt;code&gt;my_var&lt;/code&gt; and &lt;code&gt;a&lt;/code&gt; is the same.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a: \t{0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_var&rpar;&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a.b: \t{0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_var.b&rpar;&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;b.a: \t{0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_var.b.a&rpar;&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------- OUTPUT ------------------ #&lt;/span&gt;
a:     &lt;span class=&quot;hljs-number&quot;&gt;0x119554e50&lt;/span&gt;
a.b:     &lt;span class=&quot;hljs-number&quot;&gt;0x11953e680&lt;/span&gt;
b.a:     &lt;span class=&quot;hljs-number&quot;&gt;0x119554e50&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# created two variables to store the ids of a and b instances&lt;/span&gt;
a_id = id&lpar;my_var&rpar;
b_id = id&lpar;my_var.b&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;These two variables are used to store the ids of &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# printing the refernce count of a and b&lt;/span&gt;
&lt;span class=&quot;hljs-comment&quot;&gt;# printing if the object is in garbage collector or not&lt;/span&gt;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;a&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;b&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;b_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;b: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;b_id&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------------- OUTPUT -------------------- #&lt;/span&gt;
refcount&lpar;a&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
refcount&lpar;b&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
a: Object exists
b: Object exists
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, I&#39;m printing the reference count for &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;I&#39;m also checking if these objects are tracked by garbage collector or not.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you can see, the garbage collector tracked these two variables and returned &quot;Object exists&quot; for both of them as both of them are in a circular reference.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;Now, let&#39;s point &lt;code&gt;my_var&lt;/code&gt; to &lt;code&gt;None&lt;/code&gt;, so we&#39;ll only have a circular reference.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_var= &lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;a&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;b&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;b_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;b: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;b_id&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------------ OUTPUT -------------------- #&lt;/span&gt;
refcount&lpar;a&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
refcount&lpar;b&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
a: Object exists
b: Object exists
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Here, you can see that the reference count of &lt;code&gt;a&lt;/code&gt; is decreased to 1 as we changed the &lt;code&gt;my_var&lt;/code&gt; to refer to &lt;code&gt;None&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;gc.collect&lpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;a&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;refcount&lpar;b&rpar; = {0}&#39;&lt;/span&gt;.format&lpar;ref_count&lpar;b_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;a: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;a_id&rpar;&rpar;&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;b: {0}&#39;&lt;/span&gt;.format&lpar;object_by_id&lpar;b_id&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------- OUTPUT ----------------- #&lt;/span&gt;
refcount&lpar;a&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;
refcount&lpar;b&rpar; = &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;
a: Not found
b: Not found
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;We enabled the garbage collector and then the garbage collector removed both the objects and you can see that both the objects are not found.&lt;/p&gt;
&lt;h2 id=&quot;heading-object-mutability&quot;&gt;Object Mutability&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Changing the data inside the object is called modifying the internal state of the object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;An object whose internal state can be changed is called mutable otherwise it&#39;s immutable.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Immutable data types in Python are:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Numbers&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Strings&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Tuples&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Frozen Sets&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;User Defined Classes&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Mutable data types in Python are:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Lists&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Sets&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;DIctionaries&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;User-Defined Classes&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;Now, let&#39;s see some examples of mutable and immutable datatypes and understand what happens under the hood of mutable and immutable datatypes when you change their values.&lt;/p&gt;
&lt;h3 id=&quot;heading-immutable&quot;&gt;Immutable&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have a string &lt;code&gt;s = &#39;python&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;  &lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683963997841/89022a06-b180-4348-ba71-7aa8a34b25ae.png&quot; alt=&quot;s is referencing to 0x1000 where &amp;quot;python&amp;quot; is stored&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As we know, strings are immutable&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, if in the next line, you&#39;ll write &lt;code&gt;s = &#39;hello&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;First, python will create another object at some different memory address with the value &#39;hello&#39;.&lt;/p&gt;
&lt;p&gt;  &lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683964046741/920b4819-5c49-4322-af23-973f10fc8907.png&quot; alt=&quot;create new object and stored hello value&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then the variable &lt;code&gt;s&lt;/code&gt; will point to this new object&#39;s address.&lt;/p&gt;
&lt;p&gt;  &lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683964085540/20878b98-24cc-4914-903f-f8ecd8f701e7.png&quot; alt=&quot;s is not pointing to new object&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;After this, the previous object with the value &#39;python&#39; will be destroyed as no one is referencing that object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, the python memory manager will destroy the object and free up the space.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683964173422/6c7add81-667d-4bef-8165-fe0f539b634d.png&quot; alt=&quot;the old address is freed&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;s = &lt;span class=&quot;hljs-string&quot;&gt;&#39;python&#39;&lt;/span&gt;
print&lpar;s&rpar;
print&lpar;hex&lpar;id&lpar;s&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------- OUTPUT ------------------ #&lt;/span&gt;
python
&lt;span class=&quot;hljs-number&quot;&gt;0x10380b870&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;s = &lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;
print&lpar;s&rpar;
print&lpar;hex&lpar;id&lpar;s&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# -------------- OUTPUT ------------------- #&lt;/span&gt;
hello
&lt;span class=&quot;hljs-number&quot;&gt;0x106232470&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;As you can see both the addresses are different.&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-mutable&quot;&gt;Mutable&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we have a list &lt;code&gt;a = [1, 2, 3]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As we know, lists are mutable i.e. elements can be inserted, deleted and replaced.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;When we write &lt;code&gt;a = [1, 2, 3]&lt;/code&gt;, python creates an object at some memory location let&#39;s say &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;  &lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683964208562/4b192a66-8ce5-42ea-a96a-99a8c1f7be4a.png&quot; alt=&quot;a is referencing to the address 0x1000&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, &lt;code&gt;a&lt;/code&gt; points to the address &lt;code&gt;0x1000&lt;/code&gt; where the list is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say you wrote &lt;code&gt;a.append&lpar;4&rpar;&lt;/code&gt;, to append 4 in the list &lt;code&gt;a&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Unlike Immutable datatypes, python won&#39;t create a new object instead it will add the value 4 to the object that is stored in &lt;code&gt;0x1000&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1683964280809/bc6bae8a-5c68-46e0-b757-c920d2b25ff5.png&quot; alt=&quot;the list is modified and no new object is created&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# creating a list and printing out the list and it&#39;s address&lt;/span&gt;
my_list = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
print&lpar;my_list&rpar;
print&lpar;hex&lpar;id&lpar;my_list&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------------- OUTPUT ------------------ #&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
&lt;span class=&quot;hljs-number&quot;&gt;0x11bf06340&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# checking if the address is changed after modifying the list&lt;/span&gt;

my_list.append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;

print&lpar;my_list&rpar;

print&lpar;hex&lpar;id&lpar;my_list&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------------ OUTPUT -------------------- #&lt;/span&gt;
[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;]
&lt;span class=&quot;hljs-number&quot;&gt;0x11bf06340&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;You can see that the address remains the same. Let&#39;s take another example&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# creating a dictionary and printing the dictionary and it&#39;s address&lt;/span&gt;
my_dict = {&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
print&lpar;my_dict&rpar;
print&lpar;hex&lpar;id&lpar;my_dict&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ------------------ OUTPUT --------------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
&lt;span class=&quot;hljs-number&quot;&gt;0x11be9ea80&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# checking if the address is changed after modifying the dictionary&lt;/span&gt;
my_dict[&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;] = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
print&lpar;my_dict&rpar;
print&lpar;hex&lpar;id&lpar;my_dict&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------- OUTPUT ----------------- #&lt;/span&gt;
{&lt;span class=&quot;hljs-string&quot;&gt;&#39;key1&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;key2&#39;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;}
&lt;span class=&quot;hljs-number&quot;&gt;0x11be9ea80&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;As a dictionary is mutable, its address remains the same&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-mutable-datatype-within-immutable-datatype&quot;&gt;Mutable Datatype Within Immutable Datatype&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s take another tuple &lt;code&gt;b = &lpar;[1,2,3], [4,5,6]&rpar;&lt;/code&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As we know, lists are mutable i.e. elements can be inserted, deleted or replaced.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Here, we can modify the lists that are in the tuple, but we can&#39;t make nay changes to the tuple i.e we can&#39;t insert a new element to the tuple, we can&#39;t delete an element from the tuple, we can&#39;t delete element from the tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Tuple still has the same elements, but as the elements are mutable we can make changes to those elements.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;]
b = [&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;]
t = &lpar;a, b&rpar;
print&lpar;hex&lpar;id&lpar;a&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;b&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;t&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------- OUTPUT ---------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x10699f400&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x106f1dbc0&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x106f1d540&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a.append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;&rpar;
b.append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;&rpar;
print&lpar;t&rpar;
print&lpar;hex&lpar;id&lpar;a&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;b&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;t&rpar;&rpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------- OUTPUT ---------------- #&lt;/span&gt;
&lpar;[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;], [&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;]&rpar;
&lt;span class=&quot;hljs-number&quot;&gt;0x10699f400&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x106f1dbc0&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0x106f1d540&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, we only modified the lists and as they are mutable there addresses haven&#39;t changed.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We haven&#39;t modified the tuple, the tuple always had those two lists, we didn&#39;t replace, deleted or inserted anything into this tuple, that&#39;s why its address also remains the same.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-function-arguments-and-mutability&quot;&gt;Function Arguments and Mutability&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s see how the above concept of mutability and immutability affects function arguments.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;If the argument of the function is immutable, then it won&#39;t change.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;If the argument of the function is mutable, then it&#39;ll change.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s take the help of an example and understand.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-immutable-objects-as-arguments&quot;&gt;Immutable Objects as Arguments&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s create a function &lt;code&gt;process&lpar;s&rpar;&lt;/code&gt; that takes a string parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, a string is an immutable object.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# trying the similar thing with mutable and immutable objects but now the objects are passed as arguments to function&lt;/span&gt;
&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;process&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;s&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;initial s # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;s&rpar;&rpar;&rpar;&rpar;
    s = s + &lt;span class=&quot;hljs-string&quot;&gt;&#39; world&#39;&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;s after change # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;s&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;First, I printed out the memory address where the string object is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, I concatenated another string &lt;code&gt;world&lt;/code&gt; to string variable &lt;code&gt;s&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you already know, modifying immutable objects is not possible.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, first, python created another string object with this new concatenated value &lt;code&gt;&#39;hello world&#39;&lt;/code&gt;, then string variable &lt;code&gt;s&lt;/code&gt; points to the new object where the &lt;code&gt;&#39;hello world&#39;&lt;/code&gt; string is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In the end, you can see that the memory address where string variable &lt;code&gt;s&lt;/code&gt; is pointing to is now different than the previous address.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_var = &lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;my_var # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_var&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, I created a string called &lt;code&gt;my_var&lt;/code&gt; which is referencing a memory address that has an object with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Printing the memory address where the string variable &lt;code&gt;my_var&lt;/code&gt; is pointing.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;process&lpar;my_var&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Then, I called the function &lt;code&gt;process&lpar;my_var&rpar;&lt;/code&gt; and passed &lt;code&gt;my_var&lt;/code&gt; as an argument.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;my_var # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_var&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Now, you can see that the memory address of the string variable &lt;code&gt;my_var&lt;/code&gt; is still the same because &lt;code&gt;my_var&lt;/code&gt; is still pointing to the memory address where the string object with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt; is stored.&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-mutable-objects-as-arguments&quot;&gt;Mutable Objects as Arguments&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s create a function &lt;code&gt;process&lpar;items&rpar;&lt;/code&gt; that takes a list parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, a list is a mutable object.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;modify_list&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;items&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;initial items # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;items&rpar;&rpar;&rpar;&rpar;
    &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; len&lpar;items&rpar; &amp;gt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
        items[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;] = items[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;] ** &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;
    items.pop&lpar;&rpar;
    items.append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;&rpar;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;final items # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;items&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;First, I printed out the memory address where the parameter &lt;code&gt;items&lt;/code&gt; is pointing to.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, I modified every element of that list, removed an element from that list and finally append 5 to that list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you already know, modifying mutable objects is possible.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, first, python simply modified the object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In the end, you can see that the memory address where the list parameter &lt;code&gt;items&lt;/code&gt; is pointing to, is same as the previous address.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_list = [&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;]
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;my_list # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_list&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Here, I created a list &lt;code&gt;my_list&lt;/code&gt; and print out the memory address where the &lt;code&gt;my_list&lt;/code&gt; variable is pointing to.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;modify_list&lpar;my_list&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Now, I called the function &lt;code&gt;modify_list&lpar;my_list&rpar;&lt;/code&gt; with &lt;code&gt;my_list&lt;/code&gt; variable as an argument.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_list&rpar;
print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;my_list # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;my_list&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Finally, I&#39;m printing the variable &lt;code&gt;my_list&lt;/code&gt;, to check whether &lt;code&gt;my_list&lt;/code&gt; is modified or not.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;You can see that &lt;code&gt;my_list&lt;/code&gt; is modified and this makes sense as the list is mutable.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-mutable-objects-inside-mutable-objects-as-arguments&quot;&gt;Mutable Objects inside Mutable Objects as Arguments&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s create a function &lt;code&gt;modify_tuple&lpar;t&rpar;&lt;/code&gt; that takes a tuple parameter.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Remember, a tuple is an immutable object while a list is a mutable object.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;modify_tuple&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;t&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;initial t # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;t&rpar;&rpar;&rpar;&rpar;
    t[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;].append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;&rpar;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;final t # = {0}&#39;&lt;/span&gt;.format&lpar;hex&lpar;id&lpar;t&rpar;&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;First, I printed out the memory address where the parameter &lt;code&gt;t&lt;/code&gt; is pointing to.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, I modified the first element of the tuple which is a list, here I appended the value 100.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;As you already know, modifying mutable objects is possible.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, first, python simply modified the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;In the end, you can see that the memory address where the tuple parameter &lt;code&gt;t&lt;/code&gt; is pointing to, is the same as the previous address.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
b = [&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;20&lt;/span&gt;,&lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;]
my_tuple = &lpar;a,b&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;I created two lists &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; and then created a tuple &lt;code&gt;my_tuple&lt;/code&gt; containing these two lists.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;hex&lpar;id&lpar;my_tuple&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Here, I&#39;m printing the memory address where the tuple &lt;code&gt;my_tuple&lt;/code&gt; is pointing to.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;modify_tuple&lpar;my_tuple&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Now, I called the function &lt;code&gt;modify_tuple&lpar;my_tuple&rpar;&lt;/code&gt; with &lt;code&gt;my_tuple&lt;/code&gt; as an argument, that will modify the list &lt;code&gt;a&lt;/code&gt; in the tuple.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_tuple
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;You can see that the tuple&#39;s content remains the same i.e. there are two lists &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; but the list &lt;code&gt;a&lt;/code&gt; content/data is changed and it is possible as lists are mutable.&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-shared-references-and-mutability&quot;&gt;Shared References and Mutability&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Shared reference is the concept of two variables referencing the same object or same memory address.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say we create two variables &lt;code&gt;a = 10&lt;/code&gt; and &lt;code&gt;b = a&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Let&#39;s say that &lt;code&gt;a&lt;/code&gt; is pointing to the memory address &lt;code&gt;`0x1000` &lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, &lt;code&gt;b&lt;/code&gt; is also pointing to that same address.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Hence, the reference count of that address is 2.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# both the of the variables refer to the same address&lt;/span&gt;
my_var_1 = &lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;
my_var_2 = my_var_1
print&lpar;my_var_1&rpar;
print&lpar;my_var_2&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, I created two variables &lt;code&gt;my_var_1&lt;/code&gt; and &lt;code&gt;my_var_2&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_var_1&lt;/code&gt; is pointing to a memory address where an object with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt; is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;my_var_2&lt;/code&gt; is referencing &lt;code&gt;my_var_1&lt;/code&gt; which in turn points to the memory address where the object with the value &lt;code&gt;&#39;hello&#39;&lt;/code&gt; is stored.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;So, &lt;code&gt;my_var_2&lt;/code&gt; is also referencing the same memory address as &lt;code&gt;my_var_1&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, I&#39;m printing the values of both variables.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;hex&lpar;id&lpar;my_var_1&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;my_var_2&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Here, I&#39;m printing the memory address that both of these variables are pointing to.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# by modifying the address will change as string is immutable&lt;/span&gt;
my_var_2 = my_var_2 + &lt;span class=&quot;hljs-string&quot;&gt;&#39; world!&#39;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;As I modified &lt;code&gt;my_var_2&lt;/code&gt; , &lt;code&gt;my_var_2&lt;/code&gt; will point to some other location where this new object is stored.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;hex&lpar;id&lpar;my_var_1&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;my_var_2&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Now, you can see both the variables are pointing to different locations.&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;The same thing will happen with mutable objects.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# doing the same thing with mutable objects&lt;/span&gt;
my_list_1 = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]
my_list_2 = my_list_1
print&lpar;my_list_1&rpar;
print&lpar;my_list_2&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;hex&lpar;id&lpar;my_list_1&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;my_list_2&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Similarly, as above both these lists are pointing to the same location.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# it&#39;ll change both the lists as list is mutable.&lt;/span&gt;
my_list_2.append&lpar;&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Here, I&#39;m modifying the list &lt;code&gt;my_list_2&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_list_2&rpar;
print&lpar;my_list_1&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;You can see both the lists got modified as lists are mutable, so when I modified the object where the &lt;code&gt;my_list_2&lt;/code&gt; is pointing to, python didn&#39;t create another object instead python modified the same object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Due to this, both the lists are showing the modified list.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;hex&lpar;id&lpar;my_list_1&rpar;&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;my_list_2&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;You can see both lists are pointing to the same address even after modifying a list.&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-python-interning&quot;&gt;Python Interning&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In Python, interning is a technique used to optimize the use of memory by storing the commonly used objects in a cache to avoid creating new objects each time they are needed.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Two common types of objects that are interned in Python are integers and strings.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h3 id=&quot;heading-integer-interning&quot;&gt;Integer Interning&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Integer interning is the process of storing and reusing integer objects with values ranging from -5 to 256.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;When you create an integer object in this range, Python checks if it already exists in memory. If it does, it returns the reference to the existing object instead of creating a new one.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This can improve the performance of Python programs by reducing the number of objects created and the amount of memory used. For example:&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
b = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
a &lt;span class=&quot;hljs-keyword&quot;&gt;is&lt;/span&gt; b
&lt;span class=&quot;hljs-literal&quot;&gt;True&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, both &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; are assigned the integer value &lt;code&gt;10&lt;/code&gt;. Since this value is within the range of interned integers, Python interns it and assigns the same object to both &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;. Therefore, &lt;code&gt;a is b&lt;/code&gt; returns &lt;code&gt;True&lt;/code&gt;.&lt;/p&gt;
&lt;h3 id=&quot;heading-string-interning&quot;&gt;String Interning&lt;/h3&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;String interning is the process of storing and reusing string objects with the same value.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;When you create a string object in Python, it is added to a cache of commonly used strings. If another string with the same value is created, Python returns a reference to the existing object instead of creating a new one.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;This can also improve the performance of Python programs by reducing the number of objects created and the amount of memory used. For example:&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;
b = &lt;span class=&quot;hljs-string&quot;&gt;&#39;hello&#39;&lt;/span&gt;
a &lt;span class=&quot;hljs-keyword&quot;&gt;is&lt;/span&gt; b
&lt;span class=&quot;hljs-literal&quot;&gt;True&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;In this example, both &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt; are assigned the string &lt;code&gt;&#39;hello&#39;&lt;/code&gt;. Since this string is commonly used, Python interns it and assigns the same object to both &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;. Therefore, &lt;code&gt;a is b&lt;/code&gt; returns &lt;code&gt;True&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;It is important to note that interning is an implementation detail of the Python language and may vary depending on the Python interpreter being used. Therefore, it is recommended to rely on the &lt;code&gt;==&lt;/code&gt; operator to compare values of integers and strings instead of using the &lt;code&gt;is&lt;/code&gt; operator.&lt;/p&gt;
&lt;h2 id=&quot;heading-variable-equality&quot;&gt;Variable Equality&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;We can compare variables in two ways, one way is Memory address and the other one is data/content inside the object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;To compare memory addresses of variables we can use &lt;code&gt;is&lt;/code&gt; operator, which is known as an identity operator.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a is b: &quot;&lt;/span&gt;, a &lt;span class=&quot;hljs-keyword&quot;&gt;is&lt;/span&gt; b&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;To compare the data/content of the objects, we can use &lt;code&gt;==&lt;/code&gt; operator, which is known as an equality operator.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;a == b:&quot;&lt;/span&gt;, a == b&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;If you want to check if two variables memory addresses are not equal, then you can use &lt;code&gt;is not&lt;/code&gt; operator.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;If you want to check if two variable&#39;s data/content is not equal, then you can use &lt;code&gt;!=&lt;/code&gt; operator.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;The &lt;code&gt;None&lt;/code&gt; object can be assigned to variables to indicate that they are not set in the way we would expect them to be.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;For example, let&#39;s say we have a string s set to None, as we don&#39;t have any proper value, we just initialized the string with None.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a = &lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;
print&lpar;type&lpar;a&rpar;&rpar;
print&lpar;hex&lpar;id&lpar;a&rpar;&rpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;a &lt;span class=&quot;hljs-keyword&quot;&gt;is&lt;/span&gt; &lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;

&lt;span class=&quot;hljs-literal&quot;&gt;True&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;b = &lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;
hex&lpar;id&lpar;b&rpar;&rpar;

a &lt;span class=&quot;hljs-keyword&quot;&gt;is&lt;/span&gt; b
a == b
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;None object is a real object, that is managed by the Python memory manager.&lt;/li&gt;
&lt;/ul&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;hex&lpar;id&lpar;&lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;&rpar;&rpar;
type&lpar;&lt;span class=&quot;hljs-literal&quot;&gt;None&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;Python memory manager will always use a shared reference when assigning a variable to None.&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-everything-is-an-object&quot;&gt;Everything is an Object&lt;/h2&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;In Python, everything is an object. This means that any value, variable, or function in Python is considered an object.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;An object in Python is a self-contained piece of code that has data and methods that can be accessed and manipulated.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Objects are instances of classes, which are essentially blueprints that define the structure and behavior of the objects.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;For example, if you declare a variable in Python, such as:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;x = &lt;span class=&quot;hljs-number&quot;&gt;42&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;The value &lt;code&gt;42&lt;/code&gt; is an object of the &lt;code&gt;int&lt;/code&gt; class, which means it has built-in methods and attributes that can be accessed and manipulated. Similarly, if you define a function in Python, such as:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;my_function&lt;/span&gt;&lpar;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Hello, World!&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;The function &lt;code&gt;my_function&lpar;&rpar;&lt;/code&gt; is an object of the &lt;code&gt;function&lt;/code&gt; class, which means it can be passed around as a variable, returned from another function, or even assigned to a different name.&lt;/p&gt;
&lt;p&gt;The concept of everything being an object in Python is a fundamental aspect of the language and is important for understanding how Python code is executed and how objects interact with one another. It also allows for powerful programming constructs such as dynamic typing, duck typing, and metaprogramming, which can make Python code more flexible and expressive.&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Any object can be assigned to a variable, so functions&lpar;as a function is an object too&rpar; can also be assigned to a function.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Any object can be passed to a function, therefore functions can be passed to a function.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Any object can be returned from a function, therefore functions can be returned from a function.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h2 id=&quot;heading-conclusion&quot;&gt;Conclusion&lt;/h2&gt;
&lt;p&gt;In conclusion, understanding variables and their behavior in Python is crucial for writing effective and efficient code. Variables are placeholders for data that are stored in memory, and their mutability determines whether they can be changed or not. Memory management is an important consideration when working with variables, as it can impact the performance of your code. Shared references can lead to unexpected results, so it is important to be aware of how they work. Finally, understanding function argument mutability can help you avoid errors when passing variables between functions. By keeping these concepts in mind, you can write better Python code and avoid common pitfalls.&lt;/p&gt;

 <img src="$cover_image" alt="Cover Image" width="200" height="200" align="left">

## [Quick Python Primer: Master the Basics in 20 Minutes](https://neuronize.dev/quick-python-primer-master-the-basics-in-20-minutes)

&lt;p&gt;Discover the essentials of Python programming in this comprehensive review and guide, designed to help you master the basics. Learn about variables, data types, string formatting, data structures, functions, conditionals, loops, modules, and classes in Python, and unlock the power of this versatile and powerful language. Whether you&#39;re a beginner or looking to brush up on your skills, this article will provide you with a solid foundation for Python development.&lt;/p&gt;
&lt;p&gt;I&#39;ve previously discussed installing Python and setting up Visual Studio Code for Python development, so I won&#39;t explain that in this article.&lt;/p&gt;
&lt;h2 id=&quot;heading-variable&quot;&gt;Variable&lt;/h2&gt;
&lt;p&gt;In Python, a variable is a named placeholder that can store a value. Variables are created using the assignment operator &lpar;&lt;code&gt;=&lt;/code&gt;&rpar;. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_variable = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;my_variable&lt;/code&gt; is a variable that holds the value &lt;code&gt;10&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;Python has several data types that can be assigned to variables. Some common data types in Python include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;Numeric data types:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Integer &lpar;&lt;code&gt;int&lt;/code&gt;&rpar; - represents whole numbers, such as &lt;code&gt;42&lt;/code&gt; or &lt;code&gt;-7&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Float &lpar;&lt;code&gt;float&lt;/code&gt;&rpar; - represents decimal numbers, such as &lt;code&gt;3.14&lt;/code&gt; or &lt;code&gt;-0.5&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Complex &lpar;&lt;code&gt;complex&lt;/code&gt;&rpar; - represents numbers with both a real and imaginary component, such as &lt;code&gt;1 + 2j&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Boolean data type:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;Boolean &lpar;&lt;code&gt;bool&lt;/code&gt;&rpar; - represents a value of either &lt;code&gt;True&lt;/code&gt; or &lt;code&gt;False&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Sequence data types:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;String &lpar;&lt;code&gt;str&lt;/code&gt;&rpar; - represents a sequence of characters, such as &lt;code&gt;&quot;Hello, World!&quot;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;List &lpar;&lt;code&gt;list&lt;/code&gt;&rpar; - represents an ordered collection of items, such as &lt;code&gt;[1, 2, 3]&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Tuple &lpar;&lt;code&gt;tuple&lt;/code&gt;&rpar; - similar to a list, but immutable &lpar;cannot be changed&rpar;, such as &lt;code&gt;&lpar;1, 2, 3&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Mapping data type:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;Dictionary &lpar;&lt;code&gt;dict&lt;/code&gt;&rpar; - represents a collection of key-value pairs, such as &lt;code&gt;{&quot;name&quot;: &quot;John&quot;, &quot;age&quot;: 30}&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Set data type:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;Set &lpar;&lt;code&gt;set&lt;/code&gt;&rpar; - represents an unordered collection of unique items, such as &lt;code&gt;{1, 2, 3}&lt;/code&gt;.&lt;/li&gt;
&lt;/ul&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;Python is a dynamically typed language, which means that the data type of a variable is inferred at runtime based on the value it holds. For example, if you assign an integer value to a variable, the variable will have an &lt;code&gt;int&lt;/code&gt; data type. If you later assign a string value to the same variable, the variable will now have a &lt;code&gt;str&lt;/code&gt; data type.&lt;/p&gt;
&lt;h2 id=&quot;heading-string-formatting&quot;&gt;String Formatting&lt;/h2&gt;
&lt;p&gt;In Python, string formatting is the process of creating a string by inserting values into a string template. There are several ways to do string formatting in Python, including:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;Concatenation: You can concatenate strings and variables using the &lt;code&gt;+&lt;/code&gt; operator. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt; name = &lt;span class=&quot;hljs-string&quot;&gt;&quot;John&quot;&lt;/span&gt;
 age = &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
 message = &lt;span class=&quot;hljs-string&quot;&gt;&quot;My name is &quot;&lt;/span&gt; + name + &lt;span class=&quot;hljs-string&quot;&gt;&quot; and I am &quot;&lt;/span&gt; + str&lpar;age&rpar; + &lt;span class=&quot;hljs-string&quot;&gt;&quot; years old.&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt; Here, the &lt;code&gt;str&lpar;&rpar;&lt;/code&gt; function is used to convert the integer &lt;code&gt;age&lt;/code&gt; to a string so that it can be concatenated with the other strings.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;%&lt;/code&gt; operator: You can use the &lt;code&gt;%&lt;/code&gt; operator to substitute values into a string template. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt; name = &lt;span class=&quot;hljs-string&quot;&gt;&quot;John&quot;&lt;/span&gt;
 age = &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
 message = &lt;span class=&quot;hljs-string&quot;&gt;&quot;My name is %s and I am %d years old.&quot;&lt;/span&gt; % &lpar;name, age&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt; Here, &lt;code&gt;%s&lt;/code&gt; is a placeholder for a string value, and &lt;code&gt;%d&lt;/code&gt; is a placeholder for a decimal &lpar;integer&rpar; value. The values to be substituted are provided in a tuple &lt;code&gt;&lpar;name, age&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.format&lpar;&rpar;&lt;/code&gt;: You can use the &lt;code&gt;str.format&lpar;&rpar;&lt;/code&gt; method to insert values into a string template. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt; name = &lt;span class=&quot;hljs-string&quot;&gt;&quot;John&quot;&lt;/span&gt;
 age = &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
 message = &lt;span class=&quot;hljs-string&quot;&gt;&quot;My name is {} and I am {} years old.&quot;&lt;/span&gt;.format&lpar;name, age&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt; Here, the &lt;code&gt;{}&lt;/code&gt; placeholders are used to indicate where the values should be inserted. The values to be substituted are provided in the &lt;code&gt;format&lpar;&rpar;&lt;/code&gt; method.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;f-strings &lpar;formatted string literals&rpar;: This is the most recent and widely used way to format strings in Python. You can use an f-string to substitute values into a string template using curly braces &lt;code&gt;{}&lt;/code&gt;. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt; name = &lt;span class=&quot;hljs-string&quot;&gt;&quot;John&quot;&lt;/span&gt;
 age = &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
 message = &lt;span class=&quot;hljs-string&quot;&gt;f&quot;My name is &lt;span class=&quot;hljs-subst&quot;&gt;{name}&lt;/span&gt; and I am &lt;span class=&quot;hljs-subst&quot;&gt;{age}&lt;/span&gt; years old.&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt; Here, the variables &lt;code&gt;name&lt;/code&gt; and &lt;code&gt;age&lt;/code&gt; are enclosed in curly braces within the string literal, and the values will be interpolated into the string.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;In addition to string formatting, Python also provides several built-in string methods that can be used to manipulate strings. Some commonly used string methods in Python include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.upper&lpar;&rpar;&lt;/code&gt;: Converts all characters in a string to uppercase.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.lower&lpar;&rpar;&lt;/code&gt;: Converts all characters in a string to lowercase.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.strip&lpar;&rpar;&lt;/code&gt;: Removes whitespace &lpar;spaces, tabs, and newlines&rpar; from the beginning and end of a string.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.split&lpar;&rpar;&lt;/code&gt;: Splits a string into a list of substrings based on a specified separator.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.join&lpar;&rpar;&lt;/code&gt;: Joins a list of strings into a single string, using a specified separator.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.replace&lpar;&rpar;&lt;/code&gt;: Replaces all occurrences of a specified substring in a string with another substring.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.startswith&lpar;&rpar;&lt;/code&gt;: Returns &lt;code&gt;True&lt;/code&gt; if a string starts with a specified substring, otherwise &lt;code&gt;False&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;str.endswith&lpar;&rpar;&lt;/code&gt;: Returns &lt;code&gt;True&lt;/code&gt; if a string ends with a specified substring, otherwise &lt;code&gt;False&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;These are just a few of the many string methods available in Python. You can find more information on string methods in the Python documentation.&lt;/p&gt;
&lt;h2 id=&quot;heading-data-structures&quot;&gt;Data Structures&lt;/h2&gt;
&lt;h3 id=&quot;heading-list&quot;&gt;List&lt;/h3&gt;
&lt;p&gt;In Python, a list is a collection of items, which can be of any data type, that are ordered and mutable &lpar;changeable&rpar;. Lists are created by enclosing a comma-separated sequence of items within square brackets &lt;code&gt;[]&lt;/code&gt;. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_list = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;apple&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;banana&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;cherry&quot;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;my_list&lt;/code&gt; is a list that contains three integers and three strings.&lt;/p&gt;
&lt;p&gt;You can access individual items in a list by their index, which starts at 0 for the first item in the list. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_list[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 1&lt;/span&gt;
print&lpar;my_list[&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;apple&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;You can also use negative indexing to access items from the end of the list. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_list[&lt;span class=&quot;hljs-number&quot;&gt;-1&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;cherry&quot;&lt;/span&gt;
print&lpar;my_list[&lt;span class=&quot;hljs-number&quot;&gt;-3&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;apple&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Lists in Python support several built-in methods for adding, removing, and manipulating items. Some commonly used list methods include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.append&lpar;item&rpar;&lt;/code&gt;: Adds an item to the end of the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.insert&lpar;index, item&rpar;&lt;/code&gt;: Inserts an item at a specified position in the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.remove&lpar;item&rpar;&lt;/code&gt;: Removes the first occurrence of an item from the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.pop&lpar;index&rpar;&lt;/code&gt;: Removes and returns the item at a specified position in the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.sort&lpar;&rpar;&lt;/code&gt;: Sorts the items in the list in ascending order.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;list.reverse&lpar;&rpar;&lt;/code&gt;: Reverses the order of the items in the list.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;len&lpar;list&rpar;&lt;/code&gt;: Returns the number of items in the list.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;You can also use slicing to extract a subsequence of a list. Slicing uses the colon &lt;code&gt;:&lt;/code&gt; operator to specify a start index &lpar;inclusive&rpar; and end index &lpar;exclusive&rpar; for the subsequence. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_list = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;]
sub_list = my_list[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;:&lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;]  &lt;span class=&quot;hljs-comment&quot;&gt;# returns [2, 3, 4]&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Lists in Python are versatile and widely used in many applications. They can be used to store collections of data, implement algorithms, and represent complex structures.&lt;/p&gt;
&lt;h3 id=&quot;heading-tuple&quot;&gt;Tuple&lt;/h3&gt;
&lt;p&gt;In Python, a tuple is an ordered, immutable &lpar;unchangeable&rpar; collection of elements. Tuples are similar to lists, but they cannot be modified once created. Tuples are created by enclosing a comma-separated sequence of values within parentheses &lt;code&gt;&lpar;&rpar;&lt;/code&gt;. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_tuple = &lpar;&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;apple&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;banana&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;cherry&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;my_tuple&lt;/code&gt; is a tuple that contains three integers and three strings.&lt;/p&gt;
&lt;p&gt;You can access individual elements in a tuple by their index, just like in a list. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_tuple[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 1&lt;/span&gt;
print&lpar;my_tuple[&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;apple&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;However, because tuples are immutable, you cannot modify their elements once they have been created. For example, the following code will raise a &lt;code&gt;TypeError&lt;/code&gt;:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_tuple[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;] = &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;  &lt;span class=&quot;hljs-comment&quot;&gt;# raises TypeError: &#39;tuple&#39; object does not support item assignment&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Tuples in Python support several built-in methods for manipulating and querying elements. Some commonly used tuple methods include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;tuple.count&lpar;value&rpar;&lt;/code&gt;: Returns the number of times a specified value appears in the tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;tuple.index&lpar;value&rpar;&lt;/code&gt;: Returns the index of the first occurrence of a specified value in the tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;len&lpar;tuple&rpar;&lt;/code&gt;: Returns the number of elements in the tuple.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;Because tuples are immutable, they are often used to represent fixed collections of data that should not be modified, such as the coordinates of a point in 2D space or the RGB values of a color. Tuples are also commonly used to return multiple values from a function, where the values cannot be modified separately. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;get_name_and_age&lt;/span&gt;&lpar;&rpar;:&lt;/span&gt;
    name = &lt;span class=&quot;hljs-string&quot;&gt;&quot;John&quot;&lt;/span&gt;
    age = &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; name, age

result = get_name_and_age&lpar;&rpar;
print&lpar;result&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &lpar;&quot;John&quot;, 30&rpar;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, the &lt;code&gt;get_name_and_age&lpar;&rpar;&lt;/code&gt; function returns a tuple containing two values: the name and age of a person. The tuple is unpacked into the variables &lt;code&gt;result&lt;/code&gt;, which contains the two values as separate variables.&lt;/p&gt;
&lt;h3 id=&quot;heading-set&quot;&gt;Set&lt;/h3&gt;
&lt;p&gt;In Python, a set is an unordered collection of unique elements. Sets are created by enclosing a comma-separated sequence of values within curly braces &lt;code&gt;{}&lt;/code&gt; or by using the &lt;code&gt;set&lpar;&rpar;&lt;/code&gt; constructor function. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_set = {&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;my_set&lt;/code&gt; is a set that contains five unique integers.&lt;/p&gt;
&lt;p&gt;Sets in Python support several built-in methods for adding, removing, and manipulating elements. Some commonly used set methods include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.add&lpar;element&rpar;&lt;/code&gt;: Adds an element to the set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.remove&lpar;element&rpar;&lt;/code&gt;: Removes an element from the set. Raises a &lt;code&gt;KeyError&lt;/code&gt; if the element is not in the set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.discard&lpar;element&rpar;&lt;/code&gt;: Removes an element from the set if it is present. Does not raise an error if the element is not in the set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.pop&lpar;&rpar;&lt;/code&gt;: Removes and returns an arbitrary element from the set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.clear&lpar;&rpar;&lt;/code&gt;: Removes all elements from the set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.union&lpar;other_set&rpar;&lt;/code&gt;: Returns a new set that contains all elements from both sets.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.intersection&lpar;other_set&rpar;&lt;/code&gt;: Returns a new set that contains only the elements that are common to both sets.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.difference&lpar;other_set&rpar;&lt;/code&gt;: Returns a new set that contains only the elements that are in the first set but not in the second set.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;set.symmetric_difference&lpar;other_set&rpar;&lt;/code&gt;: Returns a new set that contains only the elements that are in either the first or the second set, but not both.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;len&lpar;set&rpar;&lt;/code&gt;: Returns the number of elements in the set.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;Sets in Python are often used to perform mathematical set operations such as union, intersection, and difference. They are also useful for removing duplicates from a list or other sequence. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_list = [&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;]
my_set = set&lpar;my_list&rpar;
print&lpar;my_set&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints {1, 2, 3, 4, 5}&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, the &lt;code&gt;set&lpar;&rpar;&lt;/code&gt; constructor is used to create a set from the &lt;code&gt;my_list&lt;/code&gt; list, which contains duplicate elements. The resulting set &lt;code&gt;my_set&lt;/code&gt; contains only the unique elements from &lt;code&gt;my_list&lt;/code&gt;.&lt;/p&gt;
&lt;h3 id=&quot;heading-dictionary&quot;&gt;Dictionary&lt;/h3&gt;
&lt;p&gt;In Python, a dictionary is an unordered collection of key-value pairs. Dictionaries are created by enclosing a comma-separated sequence of key-value pairs within curly braces &lt;code&gt;{}&lt;/code&gt; or by using the &lt;code&gt;dict&lpar;&rpar;&lt;/code&gt; constructor function. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_dict = {&lt;span class=&quot;hljs-string&quot;&gt;&quot;apple&quot;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;banana&quot;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;cherry&quot;&lt;/span&gt;: &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;}
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;my_dict&lt;/code&gt; is a dictionary that maps the keys &quot;apple&quot;, &quot;banana&quot;, and &quot;cherry&quot; to the values 2, 3, and 5, respectively.&lt;/p&gt;
&lt;p&gt;You can access individual values in a dictionary by their key, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;my_dict[&lt;span class=&quot;hljs-string&quot;&gt;&quot;apple&quot;&lt;/span&gt;]&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 2&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;You can also add new key-value pairs to a dictionary, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_dict[&lt;span class=&quot;hljs-string&quot;&gt;&quot;orange&quot;&lt;/span&gt;] = &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;You can modify the value associated with a key in a dictionary, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;my_dict[&lt;span class=&quot;hljs-string&quot;&gt;&quot;banana&quot;&lt;/span&gt;] = &lt;span class=&quot;hljs-number&quot;&gt;6&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;And you can remove a key-value pair from a dictionary, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;del&lt;/span&gt; my_dict[&lt;span class=&quot;hljs-string&quot;&gt;&quot;cherry&quot;&lt;/span&gt;]
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Dictionaries in Python support several built-in methods for manipulating and querying keys and values. Some commonly used dictionary methods include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.keys&lpar;&rpar;&lt;/code&gt;: Returns a view of the keys in the dictionary.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.values&lpar;&rpar;&lt;/code&gt;: Returns a view of the values in the dictionary.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.items&lpar;&rpar;&lt;/code&gt;: Returns a view of the key-value pairs in the dictionary.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.get&lpar;key, default=None&rpar;&lt;/code&gt;: Returns the value associated with a key in the dictionary, or a default value if the key is not present.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.pop&lpar;key, default=None&rpar;&lt;/code&gt;: Removes and returns the value associated with a key in the dictionary, or a default value if the key is not present.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;dict.update&lpar;other_dict&rpar;&lt;/code&gt;: Adds all key-value pairs from &lt;code&gt;other_dict&lt;/code&gt; to the dictionary, overwriting values for keys that already exist in the dictionary.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;&lt;code&gt;len&lpar;dict&rpar;&lt;/code&gt;: Returns the number of key-value pairs in the dictionary.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;Dictionaries in Python are often used to represent collections of related data where each element is identified by a unique key. They are also useful for counting the occurrences of elements in a sequence, and for performing lookups based on keys rather than indices.&lt;/p&gt;
&lt;h2 id=&quot;heading-function&quot;&gt;Function&lt;/h2&gt;
&lt;p&gt;In Python, a function is a block of reusable code that performs a specific task. Functions are defined using the &lt;code&gt;def&lt;/code&gt; keyword, followed by the function name, parentheses &lt;code&gt;&lpar;&rpar;&lt;/code&gt;, and a colon &lt;code&gt;:&lt;/code&gt;. The body of the function is indented below the function definition. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;greet&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;name&lt;/span&gt;&rpar;:&lt;/span&gt;
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Hello, &quot;&lt;/span&gt; + name + &lt;span class=&quot;hljs-string&quot;&gt;&quot;!&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;greet&lt;/code&gt; is a function that takes a parameter &lt;code&gt;name&lt;/code&gt; and prints a greeting message.&lt;/p&gt;
&lt;p&gt;You can call a function by using its name followed by parentheses, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;greet&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Alice&quot;&lt;/span&gt;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;Hello, Alice!&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Functions can have multiple parameters, and you can provide default values for some or all of the parameters. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;calculate_sum&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b=&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; a + b
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;calculate_sum&lt;/code&gt; is a function that takes two parameters, &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;, with a default value of 0 for &lt;code&gt;b&lt;/code&gt;. The function returns the sum of &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;You can call a function with default parameter values by omitting the corresponding arguments, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;calculate_sum&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;&rpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 5&lt;/span&gt;
print&lpar;calculate_sum&lpar;&lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 15&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Functions can also return values using the &lt;code&gt;return&lt;/code&gt; keyword. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;calculate_product&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;a, b&lt;/span&gt;&rpar;:&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; a * b
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Here, &lt;code&gt;calculate_product&lt;/code&gt; is a function that takes two parameters, &lt;code&gt;a&lt;/code&gt; and &lt;code&gt;b&lt;/code&gt;, and returns their product.&lt;/p&gt;
&lt;p&gt;You can call a function that returns a value and use its return value in an expression, like this:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;result = calculate_product&lpar;&lt;span class=&quot;hljs-number&quot;&gt;3&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;4&lt;/span&gt;&rpar;
print&lpar;result&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 12&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Functions in Python can be used to break down complex problems into smaller, more manageable parts, and to organize code for better readability and maintainability. They are a fundamental building block of Python programming and are used extensively in Python applications.&lt;/p&gt;
&lt;h2 id=&quot;heading-conditionals&quot;&gt;Conditionals&lt;/h2&gt;
&lt;p&gt;Conditionals in Python allow you to execute different blocks of code depending on whether certain conditions are true or false. The most commonly used conditional statement in Python is the &lt;code&gt;if&lt;/code&gt; statement.&lt;/p&gt;
&lt;p&gt;Here is an example of an &lt;code&gt;if&lt;/code&gt; statement in Python:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;x = &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; x &amp;gt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is positive&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, the &lt;code&gt;if&lt;/code&gt; statement checks whether the value of &lt;code&gt;x&lt;/code&gt; is greater than zero. If the condition is true, the &lt;code&gt;print&lt;/code&gt; statement is executed, and &quot;x is positive&quot; is printed to the console.&lt;/p&gt;
&lt;p&gt;You can also use an &lt;code&gt;else&lt;/code&gt; statement to execute a different block of code when the condition is false. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;x = &lt;span class=&quot;hljs-number&quot;&gt;-3&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; x &amp;gt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is positive&quot;&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is non-positive&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, since &lt;code&gt;x&lt;/code&gt; is negative, the &lt;code&gt;if&lt;/code&gt; condition is false, and the &lt;code&gt;else&lt;/code&gt; block is executed instead. &quot;x is non-positive&quot; is printed to the console.&lt;/p&gt;
&lt;p&gt;You can also use an &lt;code&gt;elif&lt;/code&gt; &lpar;short for &quot;else if&quot;&rpar; statement to test additional conditions after the initial &lt;code&gt;if&lt;/code&gt; statement. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;x = &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; x &amp;gt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is positive&quot;&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-keyword&quot;&gt;elif&lt;/span&gt; x &amp;lt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is negative&quot;&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is zero&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, since &lt;code&gt;x&lt;/code&gt; is zero, the first &lt;code&gt;if&lt;/code&gt; condition is false, and the &lt;code&gt;elif&lt;/code&gt; condition is tested instead. Since &lt;code&gt;x&lt;/code&gt; is not negative either, the &lt;code&gt;else&lt;/code&gt; block is executed instead. &quot;x is zero&quot; is printed to the console.&lt;/p&gt;
&lt;p&gt;Conditionals in Python can also use logical operators such as &lt;code&gt;and&lt;/code&gt;, &lt;code&gt;or&lt;/code&gt;, and &lt;code&gt;not&lt;/code&gt; to combine multiple conditions. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;x = &lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; x &amp;gt; &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;and&lt;/span&gt; x &amp;lt; &lt;span class=&quot;hljs-number&quot;&gt;100&lt;/span&gt;:
    print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;x is a positive two-digit number&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, the &lt;code&gt;if&lt;/code&gt; condition checks whether &lt;code&gt;x&lt;/code&gt; is both greater than zero and less than 100. If the condition is true, the &lt;code&gt;print&lt;/code&gt; statement is executed.&lt;/p&gt;
&lt;p&gt;Conditionals in Python are a powerful tool for controlling program flow and making decisions based on different situations. They are used extensively in Python programs to implement logic and make decisions based on user input, data values, and other factors.&lt;/p&gt;
&lt;h2 id=&quot;heading-loops&quot;&gt;Loops&lt;/h2&gt;
&lt;p&gt;In Python, loops allow you to execute a block of code multiple times. There are two types of loops in Python: &lt;code&gt;for&lt;/code&gt; loops and &lt;code&gt;while&lt;/code&gt; loops.&lt;/p&gt;
&lt;p&gt;A &lt;code&gt;for&lt;/code&gt; loop is used to iterate over a sequence of values, such as a list or a string. Here is an example of a &lt;code&gt;for&lt;/code&gt; loop in Python:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;fruits = [&lt;span class=&quot;hljs-string&quot;&gt;&quot;apple&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;banana&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;cherry&quot;&lt;/span&gt;]
&lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; fruit &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; fruits:
    print&lpar;fruit&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, the &lt;code&gt;for&lt;/code&gt; loop iterates over the list of fruits and prints each one to the console.&lt;/p&gt;
&lt;p&gt;A &lt;code&gt;while&lt;/code&gt; loop is used to execute a block of code repeatedly as long as a certain condition is true. Here is an example of a &lt;code&gt;while&lt;/code&gt; loop in Python:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;i = &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;
&lt;span class=&quot;hljs-keyword&quot;&gt;while&lt;/span&gt; i &amp;lt; &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;:
    print&lpar;i&rpar;
    i += &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, the &lt;code&gt;while&lt;/code&gt; loop prints the value of &lt;code&gt;i&lt;/code&gt; to the console and increments it by 1 each time, until &lt;code&gt;i&lt;/code&gt; is no longer less than 5.&lt;/p&gt;
&lt;p&gt;You can also use the &lt;code&gt;break&lt;/code&gt; and &lt;code&gt;continue&lt;/code&gt; statements to control the flow of a loop. The &lt;code&gt;break&lt;/code&gt; statement allows you to exit a loop prematurely, while the &lt;code&gt;continue&lt;/code&gt; statement allows you to skip over certain iterations of a loop. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; i &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; range&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;:
    &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; i == &lt;span class=&quot;hljs-number&quot;&gt;5&lt;/span&gt;:
        &lt;span class=&quot;hljs-keyword&quot;&gt;break&lt;/span&gt;
    &lt;span class=&quot;hljs-keyword&quot;&gt;elif&lt;/span&gt; i % &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt; == &lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;:
        &lt;span class=&quot;hljs-keyword&quot;&gt;continue&lt;/span&gt;
    print&lpar;i&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, the &lt;code&gt;for&lt;/code&gt; loop prints the values of &lt;code&gt;i&lt;/code&gt; from 0 to 9, but it uses the &lt;code&gt;break&lt;/code&gt; statement to exit the loop prematurely when &lt;code&gt;i&lt;/code&gt; is equal to 5. It also uses the &lt;code&gt;continue&lt;/code&gt; statement to skip over even values of &lt;code&gt;i&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;Loops in Python are a powerful tool for iterating over sequences of values, executing code repeatedly, and controlling program flow. They are used extensively in Python programs to implement logic and perform tasks such as data processing, file I/O, and user interaction.&lt;/p&gt;
&lt;h2 id=&quot;heading-module&quot;&gt;Module&lt;/h2&gt;
&lt;p&gt;In Python, a module is a file containing Python code that can be imported into other Python scripts or modules. Modules provide a way to organize code into reusable units and avoid name collisions between different parts of a program.&lt;/p&gt;
&lt;p&gt;To use a module in Python, you simply import it using the &lt;code&gt;import&lt;/code&gt; statement. Here is an example of how to import the &lt;code&gt;math&lt;/code&gt; module, which provides mathematical functions such as trigonometric and logarithmic functions:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; math

print&lpar;math.sqrt&lpar;&lt;span class=&quot;hljs-number&quot;&gt;25&lt;/span&gt;&rpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 5.0&lt;/span&gt;
print&lpar;math.sin&lpar;math.pi / &lt;span class=&quot;hljs-number&quot;&gt;2&lt;/span&gt;&rpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 1.0&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, we import the &lt;code&gt;math&lt;/code&gt; module and use its &lt;code&gt;sqrt&lt;/code&gt; and &lt;code&gt;sin&lt;/code&gt; functions to calculate the square root of 25 and the sine of pi/2, respectively.&lt;/p&gt;
&lt;p&gt;You can also import specific functions or variables from a module using the &lt;code&gt;from&lt;/code&gt; keyword. For example:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;from&lt;/span&gt; math &lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; sqrt, pi

print&lpar;sqrt&lpar;&lt;span class=&quot;hljs-number&quot;&gt;25&lt;/span&gt;&rpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 5.0&lt;/span&gt;
print&lpar;pi&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints 3.141592653589793&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, we import only the &lt;code&gt;sqrt&lt;/code&gt; and &lt;code&gt;pi&lt;/code&gt; functions from the &lt;code&gt;math&lt;/code&gt; module, which allows us to use them directly without having to prefix them with &lt;code&gt;math.&lt;/code&gt;.&lt;/p&gt;
&lt;p&gt;Python also comes with a large standard library of modules that provide a wide range of functionality, such as file I/O, network communication, and GUI programming. In addition, there are many third-party modules available from the Python Package Index &lpar;PyPI&rpar; that can be installed using the &lt;code&gt;pip&lt;/code&gt; package manager.&lt;/p&gt;
&lt;p&gt;Modules in Python are a powerful tool for organizing and reusing code, and they provide a convenient way to extend the functionality of the language. By importing modules, you can leverage existing code and focus on solving your specific programming problems.&lt;/p&gt;
&lt;h2 id=&quot;heading-classes-and-objects&quot;&gt;Classes and Objects&lt;/h2&gt;
&lt;p&gt;In Python, a class is a blueprint or template for creating objects, which are instances of the class. A class defines a set of attributes and methods that describe the behavior of objects created from that class.&lt;/p&gt;
&lt;p&gt;Here is an example of a simple class in Python:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-class&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;Person&lt;/span&gt;:&lt;/span&gt;
    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;__init__&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;self, name, age&lt;/span&gt;&rpar;:&lt;/span&gt;
        self.name = name
        self.age = age

    &lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;say_hello&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;self&lt;/span&gt;&rpar;:&lt;/span&gt;
        print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;f&quot;Hello, my name is &lt;span class=&quot;hljs-subst&quot;&gt;{self.name}&lt;/span&gt; and I am &lt;span class=&quot;hljs-subst&quot;&gt;{self.age}&lt;/span&gt; years old.&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, we define a &lt;code&gt;Person&lt;/code&gt; class with two attributes &lpar;&lt;code&gt;name&lt;/code&gt; and &lt;code&gt;age&lt;/code&gt;&rpar; and one method &lpar;&lt;code&gt;say_hello&lt;/code&gt;&rpar;. The &lt;code&gt;__init__&lt;/code&gt; method is a special method that is called when an object of the class is created. It initializes the &lt;code&gt;name&lt;/code&gt; and &lt;code&gt;age&lt;/code&gt; attributes with the values passed as arguments.&lt;/p&gt;
&lt;p&gt;To create an object from the &lt;code&gt;Person&lt;/code&gt; class, we can use the following syntax:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;person1 = Person&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Alice&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;25&lt;/span&gt;&rpar;
person2 = Person&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Bob&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;30&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, we create two objects &lpar;&lt;code&gt;person1&lt;/code&gt; and &lt;code&gt;person2&lt;/code&gt;&rpar; from the &lt;code&gt;Person&lt;/code&gt; class with different values for the &lt;code&gt;name&lt;/code&gt; and &lt;code&gt;age&lt;/code&gt; attributes.&lt;/p&gt;
&lt;p&gt;We can call the &lt;code&gt;say_hello&lt;/code&gt; method on each object to display a greeting:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;person1.say_hello&lpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;Hello, my name is Alice and I am 25 years old.&quot;&lt;/span&gt;
person2.say_hello&lpar;&rpar;  &lt;span class=&quot;hljs-comment&quot;&gt;# prints &quot;Hello, my name is Bob and I am 30 years old.&quot;&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;In this example, we call the &lt;code&gt;say_hello&lt;/code&gt; method on each object to display a personalized greeting.&lt;/p&gt;
&lt;p&gt;Classes and objects are a fundamental concept in object-oriented programming &lpar;OOP&rpar; and are used extensively in Python programs to organize code and implement complex systems. By defining classes, you can create reusable code that can be easily modified and extended, and by creating objects, you can model real-world entities and manipulate them in your program.&lt;/p&gt;
&lt;h2 id=&quot;heading-conclusion&quot;&gt;Conclusion&lt;/h2&gt;
&lt;p&gt;In conclusion, Python is a versatile and powerful programming language with a wide range of features and applications. By mastering the basics, such as variables, data types, string formatting, data structures, functions, conditionals, loops, modules, and classes, you can unlock the full potential of Python and become a proficient developer. Whether you are a beginner or looking to enhance your skills, understanding these fundamental concepts will provide a strong foundation for your Python development journey.&lt;/p&gt;
&lt;p&gt;In this series, you&#39;ll be learning Python in-depth starting from variables to Object Oriented Programming. At the end of this series, you&#39;ll be a proficient Python programmer, who&#39;ll know how to write optimized code.&lt;/p&gt;

 <img src="$cover_image" alt="Cover Image" width="200" height="200" align="left">

## [Beginner&#39;s Guide to Python: A Comprehensive Overview](https://neuronize.dev/beginners-guide-to-python-a-comprehensive-overview)

&lt;p&gt;Python is a popular high-level programming language that was created by Guido van Rossum in the late 1980s. It is an interpreted language, which means that it does not need to be compiled like some other programming languages. Python&#39;s syntax is designed to be easy to read and write, making it a popular choice for beginners. Python is a versatile language that can be used for a wide range of applications, including web development, data analysis, machine learning, and scientific computing. It has a rich ecosystem of libraries and frameworks that make it easy to extend the language&#39;s functionality and perform complex tasks with relatively little effort. Python&#39;s popularity and ease of use have made it a popular choice for programmers and data scientists alike.&lt;/p&gt;
&lt;h2 id=&quot;heading-setup-python-and-vs-code&quot;&gt;Setup Python and VS Code&lt;/h2&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;Install Python: The first step to setting up Python is to download and install Python on your computer. You can download the latest version of Python from the official website at &lt;a target=&quot;_blank&quot; href=&quot;https://www.python.org/downloads/&quot;&gt;https://www.python.org/downloads/&lt;/a&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Install Visual Studio Code: Visual Studio Code &lpar;VS Code&rpar; is a popular open-source code editor that is used for Python development. You can download VS Code from the official website at &lt;a target=&quot;_blank&quot; href=&quot;https://code.visualstudio.com/download&quot;&gt;https://code.visualstudio.com/download&lt;/a&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Install the Python extension for VS Code: Once you have installed VS Code, the next step is to install the Python extension for VS Code. This extension provides syntax highlighting, code completion, debugging, and other features specific to Python development. To install the Python extension, open VS Code and click on the Extensions icon in the sidebar &lpar;or press Ctrl + Shift + X&rpar;. Search for &quot;Python&quot; in the extensions marketplace, and click Install.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Configure VS Code for Python: After installing the Python extension, you need to configure VS Code to use your installed version of Python. To do this, open VS Code and go to the Command Palette &lpar;View -&amp;gt; Command Palette, or press Ctrl + Shift + P&rpar;. Type &quot;Python: Select Interpreter&quot; and press Enter. This will open a list of available Python interpreters on your system. Select the version of Python you installed in step 1.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Create a new Python project: To start writing Python code in VS Code, you need to create a new Python project. Open VS Code and click File -&amp;gt; New Folder to create a new folder for your project. Then, open the folder in VS Code by clicking File -&amp;gt; Open Folder. In the Explorer panel, right-click on the folder and select &quot;New File&quot;. Name the file &quot;&lt;a target=&quot;_blank&quot; href=&quot;http://main.py&quot;&gt;main.py&lt;/a&gt;&quot; &lpar;or any other name you prefer&rpar; and press Enter. This will create a new Python file in your project.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Write Python code in VS Code: With your Python project set up in VS Code, you can start writing Python code. Open the &lt;a target=&quot;_blank&quot; href=&quot;http://main.py&quot;&gt;main.py&lt;/a&gt; file, and type the following code:&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;print&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;Hello, World!&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Save the file &lpar;Ctrl + S&rpar;, then open the Terminal in VS Code &lpar;View -&amp;gt; Terminal, or press Ctrl + `&rpar;. Type the following command to run the Python file:&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-bash&quot;&gt;python main.py
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;You should see the output &quot;Hello, World!&quot; in the Terminal.&lt;/p&gt;
&lt;p&gt;Congratulations, you have set up Python and VS Code for Python development!&lt;/p&gt;
&lt;h2 id=&quot;heading-python-libraries&quot;&gt;Python Libraries&lt;/h2&gt;
&lt;p&gt;Python libraries, also known as modules, are collections of pre-written code that provide additional functionality to the Python programming language. Libraries can be used to perform a wide variety of tasks, from scientific computing and data analysis to web development and game programming.&lt;/p&gt;
&lt;p&gt;Python comes with a number of built-in libraries, such as &quot;math&quot; for mathematical operations and &quot;random&quot; for generating random numbers. However, there are also many third-party libraries available that can be downloaded and used in your Python code.&lt;/p&gt;
&lt;p&gt;Some popular third-party libraries include:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;NumPy: NumPy is a library used for scientific computing in Python. It provides support for large, multi-dimensional arrays and matrices, as well as a variety of mathematical operations and functions.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Pandas: Pandas is a library used for data analysis and manipulation in Python. It provides tools for importing, cleaning, and transforming data, as well as statistical analysis and visualization.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Matplotlib: Matplotlib is a library used for data visualization in Python. It provides tools for creating a wide variety of graphs and charts, including scatter plots, line charts, and histograms.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Flask: Flask is a library used for building web applications in Python. It provides a lightweight framework for creating web pages and handling HTTP requests and responses.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Pygame: Pygame is a library used for game development in Python. It provides tools for creating 2D games, including graphics, sound, and input handling.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;These are just a few examples of the many libraries available for Python. By using libraries, Python programmers can save time and effort by building on existing code instead of starting from scratch and can take advantage of the expertise and knowledge of other developers in the Python community.&lt;/p&gt;
&lt;h2 id=&quot;heading-python-applications&quot;&gt;Python Applications&lt;/h2&gt;
&lt;p&gt;Python is a versatile programming language that can be used to build a wide variety of applications. Here are a few examples of Python applications:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;Web Applications: Python is commonly used for building web applications, thanks to its ease of use and a wide variety of web frameworks like Flask, Django, Pyramid, and others. These frameworks allow developers to build websites, APIs, and web-based software easily.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Scientific Computing: Python is popular for scientific computing because of its libraries like NumPy, SciPy, Matplotlib, and pandas, which enable developers to perform complex mathematical calculations and data analysis.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Machine Learning and AI: Python has become one of the most popular programming languages for building machine learning and artificial intelligence applications. With libraries such as TensorFlow, Keras, PyTorch, and Scikit-learn, developers can build complex neural networks and deep learning models.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Desktop Applications: Python can be used for building desktop applications using frameworks such as PyQt, Kivy, and wxPython. These frameworks provide the tools for building user interfaces, event handling, and more.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Games: Python can also be used for game development with libraries such as Pygame and PyOpenGL. Pygame is a library designed specifically for building 2D games, while PyOpenGL can be used for building 3D games.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Automation: Python is widely used for automation tasks such as testing, data extraction, and data processing. With libraries such as Selenium, PyAutoGUI, and Beautiful Soup, developers can automate a wide variety of tasks.&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;These are just a few examples of the many applications of Python. With its ease of use, flexibility, and the vast library support, Python has become a popular choice for a wide range of programming tasks.&lt;/p&gt;
&lt;h2 id=&quot;heading-conclusion&quot;&gt;Conclusion&lt;/h2&gt;
&lt;p&gt;In conclusion, Python is a powerful and versatile programming language that can be used for a wide range of applications. Its simplicity, ease of use, and the vast range of libraries make it an attractive option for beginners as well as experienced developers. Whether you are building a web application, a scientific computing program, a machine learning model, or a game, Python provides the tools and libraries to make the development process easier and faster. Additionally, Python&#39;s popularity and community support mean that there is a wealth of resources available online, making it easy to learn and troubleshoot. Overall, Python is an excellent choice for anyone looking to get started in programming or to expand their skillset.&lt;/p&gt;

 <img src="$cover_image" alt="Cover Image" width="200" height="200" align="left">

## [Zomato EDA: Insights into Indian Food Industry Trends](https://neuronize.dev/zomato-eda-insights-into-indian-food-industry-trends)

&lt;p&gt;Zomato is one of the most popular online food delivery platforms in India. But what can we learn from the data that Zomato collects and shares? In this blog post, I will explore some interesting insights from the Zomato dataset using exploratory data analysis &lpar;EDA&rpar;. EDA is a process of summarizing, visualizing, and understanding the data before applying any machine learning or statistical techniques. It can help us discover patterns, trends, outliers, and anomalies in the data. Let&#39;s get started!&lt;/p&gt;
&lt;p&gt;Dataset -- &lt;a target=&quot;_blank&quot; href=&quot;https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants&quot;&gt;https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants&lt;/a&gt;&lt;/p&gt;
&lt;h1 id=&quot;heading-prerequisites&quot;&gt;Prerequisites&lt;/h1&gt;
&lt;p&gt;Before going forward, make sure you have covered the prerequisites, if not then you can check out my articles on those libraries:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Pandas --&amp;gt; &lt;a target=&quot;_blank&quot; href=&quot;https://neuronize.dev/pandas-101-learn-pandas-in-10-minutes&quot;&gt;Click Here To Learn Pandas in 10 minutes&lt;/a&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Matplotlib --&amp;gt; &lt;a target=&quot;_blank&quot; href=&quot;https://neuronize.dev/matplotlib-101-learn-matplotlib-in-10-minutes&quot;&gt;Click Here To Learn Matplotlib in 10 minutes&lt;/a&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Seaborn --&amp;gt; &lt;a target=&quot;_blank&quot; href=&quot;https://neuronize.dev/seaborn-101-learn-seaborn-in-10-minutes&quot;&gt;Click Here To Learn Seaborn in 10 minutes&lt;/a&gt;&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;h1 id=&quot;heading-importing-libraries&quot;&gt;Importing Libraries&lt;/h1&gt;
&lt;p&gt;Let&#39;s import all the libraries that we need.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; pandas &lt;span class=&quot;hljs-keyword&quot;&gt;as&lt;/span&gt; pd

&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; numpy &lt;span class=&quot;hljs-keyword&quot;&gt;as&lt;/span&gt; np

&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; matplotlib.pyplot &lt;span class=&quot;hljs-keyword&quot;&gt;as&lt;/span&gt; plt

&lt;span class=&quot;hljs-keyword&quot;&gt;import&lt;/span&gt; seaborn &lt;span class=&quot;hljs-keyword&quot;&gt;as&lt;/span&gt; sns

sns.set_style&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;dark&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;h1 id=&quot;heading-load-the-data&quot;&gt;Load the Data&lt;/h1&gt;
&lt;p&gt;First, let&#39;s load the data.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df = pd.read_csv&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;zomato.csv&quot;&lt;/span&gt;&rpar;
df
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681737573487/3bbc7838-5ca6-4e4e-83b5-76b6af796051.png&quot; alt=&quot;zomato dataset&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;h2 id=&quot;heading-check-the-shape-of-the-data&quot;&gt;Check the Shape of the Data&lt;/h2&gt;
&lt;p&gt;Now, let&#39;s check how many rows and columns are there in this dataset.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df.shape

&lt;span class=&quot;hljs-comment&quot;&gt;#--------------------- OUTPUT------------------------#&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-number&quot;&gt;51717&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;17&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-comment&quot;&gt;#--------------------- OUTPUT------------------------#&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;h2 id=&quot;heading-list-all-the-columns&quot;&gt;List all the Columns&lt;/h2&gt;
&lt;p&gt;Now, we&#39;ll find out all the columns of this dataset.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df.columns

&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------------- OUTPUT -------------------- #&lt;/span&gt;
Index&lpar;[&lt;span class=&quot;hljs-string&quot;&gt;&#39;url&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;address&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;name&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;online_order&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;book_table&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;rate&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;votes&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;phone&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;location&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;rest_type&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;dish_liked&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;cuisines&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;approx_cost&lpar;for two people&rpar;&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;reviews_list&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;menu_item&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;listed_in&lpar;type&rpar;&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;listed_in&lpar;city&rpar;&#39;&lt;/span&gt;], dtype=&lt;span class=&quot;hljs-string&quot;&gt;&#39;object&#39;&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-comment&quot;&gt;# ----------------------- OUTPUT -------------------- #&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Now, let&#39;s start data preprocessing.&lt;/p&gt;
&lt;h1 id=&quot;heading-data-preprocessing&quot;&gt;Data Preprocessing&lt;/h1&gt;
&lt;p&gt;First, let&#39;s see all the columns, their data type and how many non-null values are there in each column.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df.info&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681737656497/26daff2a-efe4-4748-a5ce-5cf440075468.png&quot; alt=&quot;zomato dataset info&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;You can see that there are a total of 51717 entries or rows and most of the columns have no null values and there&#39;s only one column with &lt;code&gt;int&lt;/code&gt; datatype. The total size of the dataset is 6.7+ MB.&lt;/p&gt;
&lt;p&gt;Now, we&#39;ll remove all the columns that we don&#39;t need for this analysis. If you want to keep them, then feel free to use them in your analysis but for this article, I won&#39;t be using them, so I&#39;ll just simply delete them for now.&lt;/p&gt;
&lt;h3 id=&quot;heading-deleting-columns&quot;&gt;Deleting Columns&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;#removing url column, address column, last column&lt;/span&gt;

df.drop&lpar;columns=[&lt;span class=&quot;hljs-string&quot;&gt;&quot;url&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;address&quot;&lt;/span&gt;,&lt;span class=&quot;hljs-string&quot;&gt;&quot;phone&quot;&lt;/span&gt;,&lt;span class=&quot;hljs-string&quot;&gt;&quot;menu_item&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;reviews_list&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;listed_in&lpar;city&rpar;&quot;&lt;/span&gt;], inplace=&lt;span class=&quot;hljs-literal&quot;&gt;True&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;code&gt;drop&lt;/code&gt; function is used whenever we want to delete a row or column. Here, the &lt;code&gt;drop&lt;/code&gt; function takes two parameters. &lt;code&gt;columns&lt;/code&gt; is used to specify which columns we want to delete and &lt;code&gt;inplace&lt;/code&gt; is used to modify the original dataset &lt;code&gt;df&lt;/code&gt; in place.&lt;/p&gt;
&lt;p&gt;Let&#39;s take a look at the data after dropping the columns.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681737806989/cdbf9506-dde9-4dd6-ae47-b929d1378f47.png&quot; alt=&quot;dropped columns from the dataset&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;Now, let&#39;s see the shape of the data.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df.shape

&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------------- OUTPUT ---------------- #&lt;/span&gt;
&lpar;&lt;span class=&quot;hljs-number&quot;&gt;51717&lt;/span&gt;, &lt;span class=&quot;hljs-number&quot;&gt;11&lt;/span&gt;&rpar;
&lt;span class=&quot;hljs-comment&quot;&gt;# ---------------------- OUTPUT ---------------- #&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;You can see that the changes are in-place i.e the columns from the original data frame &lt;code&gt;df&lt;/code&gt; got deleted.&lt;/p&gt;
&lt;p&gt;Now, let&#39;s preprocess some columns.&lt;/p&gt;
&lt;h2 id=&quot;heading-rate-column&quot;&gt;Rate Column&lt;/h2&gt;
&lt;p&gt;In the above data frame figure, we want to remove the &lt;code&gt;/5&lt;/code&gt; in every rating and we also need to check if there are null values or not, there also can be some weird or garbage values. So, let&#39;s start cleaning the &lt;code&gt;rate&lt;/code&gt; column.&lt;/p&gt;
&lt;p&gt;First, we&#39;ll check all the unique values in the &lt;code&gt;rate&lt;/code&gt; column, this will help us to know if there are null values or not and also if there are garbage values or not.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;].unique&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681737939759/fd67fc27-3030-4168-8d10-323e1103f0a8.png&quot; alt=&quot;all the unique values in the rate column&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;You can see that, there is a garbage value that is &quot;NEW&quot; and &quot;-&quot; and null values are also there as a &lt;code&gt;nan&lt;/code&gt; is there.&lt;/p&gt;
&lt;p&gt;So, let&#39;s start by removing the garbage values replacing them with null values and removing the &quot;/5&quot; from all the valid ratings.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# remove NEW, -, /5 from the rating&lt;/span&gt;

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;rate_handler&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;value&lt;/span&gt;&rpar;:&lt;/span&gt;

    &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; value == &lt;span class=&quot;hljs-string&quot;&gt;&quot;NEW&quot;&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;or&lt;/span&gt; value == &lt;span class=&quot;hljs-string&quot;&gt;&quot;-&quot;&lt;/span&gt;:

        &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; np.nan

    &lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:

        value = str&lpar;value&rpar;.split&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;/&#39;&lt;/span&gt;&rpar;

        value = value[&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;]

    &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; float&lpar;value&rpar;

df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;] = df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;].apply&lpar;rate_handler&rpar;

df.head&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681738054157/83059016-1b51-40da-b64f-7d7fa8618e64.png&quot; alt=&quot;dataset after removing the garbage values of rate column&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;Now, let&#39;s check all the unique values again to confirm that the garbage values and the &quot;/5&quot; are completely removed.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df.unique&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1681738139261/ff3a82c7-6dc5-4419-8dfb-db6a15ff8254.png&quot; alt=&quot;all the unique values of rate column after removing garbage values&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;This confirms that there are no garbage values and no /5.&lt;/p&gt;
&lt;p&gt;Now let&#39;s fill the null values with the average rating of all the restaurants. You can use different strategies but I&#39;ll go with this one.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;#handling missing rate values&lt;/span&gt;

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;missing_value_handler&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;column&lt;/span&gt;&rpar;:&lt;/span&gt;

    df[column].fillna&lpar;df[column].mean&lpar;&rpar;, inplace=&lt;span class=&quot;hljs-literal&quot;&gt;True&lt;/span&gt;&rpar;

missing_value_handler&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Now, let&#39;s check if there are null values present or not in the rate column.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;].isnull&lpar;&rpar;.sum&lpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# --------------------- OUTPUT --------------------- #&lt;/span&gt;
&lt;span class=&quot;hljs-number&quot;&gt;0&lt;/span&gt;
&lt;span class=&quot;hljs-comment&quot;&gt;# --------------------- OUTPUT --------------------- #&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;So, this confirms that there are no null values and we have cleaned the &lt;code&gt;rate&lt;/code&gt; column.&lt;/p&gt;
&lt;h2 id=&quot;heading-approxcostfor-two-people-column&quot;&gt;approx_cost&lpar;for two people&rpar; Column&lt;/h2&gt;
&lt;p&gt;Similarly, let&#39;s check all the unique values to know if there are null and garbage values present in the column or not.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;approx_cost&lpar;for two people&rpar;&quot;&lt;/span&gt;].unique&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078220975/e2d57686-b58a-416c-a3d4-1affc68c5467.png&quot; alt=&quot;all the unique cost values&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;You can see that cost values having 4 digits consist of a &quot;,&quot; and we don&#39;t want that, so let&#39;s remove the &quot;,&quot;.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# remove the comma&lt;/span&gt;

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;cost_handler&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;value&lt;/span&gt;&rpar;:&lt;/span&gt;

    value = str&lpar;value&rpar;

    &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;hljs-string&quot;&gt;&#39;,&#39;&lt;/span&gt; &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; value:

        value = value.replace&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;,&#39;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&#39;&#39;&lt;/span&gt;&rpar;

        &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; float&lpar;value&rpar;

    &lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:

        &lt;span class=&quot;hljs-keyword&quot;&gt;return&lt;/span&gt; float&lpar;value&rpar;



df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;approx_cost&lpar;for two people&rpar;&quot;&lt;/span&gt;] = df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;approx_cost&lpar;for two people&rpar;&quot;&lt;/span&gt;].apply&lpar;cost_handler&rpar;

df.head&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, the function &lt;code&gt;cost_handler&lpar;&rpar;&lt;/code&gt; takes an argument value which is the cost.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then we are converting the cost to string so that we can do string manipulation.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, we are saying if the cost string consists &quot;,&quot; then replace it with an empty string.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, we are typecasting the string to float and returning the value.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;The &lt;code&gt;apply&lpar;&rpar;&lt;/code&gt; function can be used to apply a function to every value in a pandas series or data frame. Here, we are applying the &lt;code&gt;cost_handler&lpar;&rpar;&lt;/code&gt; function to the &lt;code&gt;df&lt;/code&gt; data frame.&lt;/p&gt;
&lt;p&gt;Now, let&#39;s take a look at all the unique values again just to confirm that we have removed all the commas.&lt;/p&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;approx_cost&lpar;for two people&rpar;&quot;&lt;/span&gt;].unique&lpar;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078345021/e52854c5-286c-40dc-a6c1-e917f136151b.png&quot; alt /&gt;&lt;/p&gt;
&lt;p&gt;You can see that all the commas in the 4-digit cost have been removed.&lt;/p&gt;
&lt;p&gt;If you want to can fill in the null values in the &lt;code&gt;cost&lt;/code&gt; column but I&#39;m not going to do that for this analysis.&lt;/p&gt;
&lt;h1 id=&quot;heading-eda&quot;&gt;EDA&lt;/h1&gt;
&lt;p&gt;Now, let&#39;s start to ask some questions and try to get the answers with visualization.&lt;/p&gt;
&lt;p&gt;These are the 5 questions that we&#39;ll try to answer and visualize:&lt;/p&gt;
&lt;ol&gt;
&lt;li&gt;&lt;p&gt;Number of restaurants having online order facility&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Top 10 best-rated restaurants&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Top 10 cuisines served by restaurants&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Number of Restaurants in every location&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Top 10 liked dishes&lt;/p&gt;
&lt;/li&gt;
&lt;/ol&gt;
&lt;h3 id=&quot;heading-number-of-restaurants-having-online-order-facility&quot;&gt;Number of restaurants having online order facility&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;sns.countplot&lpar;df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;online_order&quot;&lt;/span&gt;]&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078421449/056c7b9b-713a-4500-829b-85ddc772ad41.png&quot; alt=&quot;number of restaurants having online order facility&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;Most restaurants provide online order service, and nearly 30,000 restaurants provide online order service. To find the exact number you can use pandas &lt;code&gt;value_counts&lt;/code&gt; to get the count for each of the option &lt;code&gt;yes&lt;/code&gt; and &lt;code&gt;no&lt;/code&gt;.&lt;/p&gt;
&lt;h3 id=&quot;heading-top-10-best-rated-restaurants&quot;&gt;Top 10 best-rated restaurants&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# top 10 rated restaurants&lt;/span&gt;

df.groupby&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;name&quot;&lt;/span&gt;&rpar;[&lt;span class=&quot;hljs-string&quot;&gt;&quot;rate&quot;&lt;/span&gt;].mean&lpar;&rpar;.sort_values&lpar;ascending=&lt;span class=&quot;hljs-literal&quot;&gt;False&lt;/span&gt;&rpar;.head&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, we are grouping the data concerning &lt;code&gt;name&lt;/code&gt; of restaurants.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then finds the mean of all the ratings for that particular restaurant.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, we are sorting the output of the above in decreasing order to get the highest ratings and then retrieving the top 10 data using &lt;code&gt;head&lpar;10&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078483340/9deea75b-3644-43cd-a4c1-e0c26a7cb046.png&quot; alt=&quot;top 10 best-rated restaurants&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;h3 id=&quot;heading-top-10-cuisines-served&quot;&gt;Top 10 Cuisines Served&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# top 10 cousines served by restaurants&lt;/span&gt;

cousines = {}

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;cousines_handler&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;value&lt;/span&gt;&rpar;:&lt;/span&gt;

    value = str&lpar;value&rpar;.split&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;,&#39;&lt;/span&gt;&rpar;

    &lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; cousine &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; value:

        cousine = cousine.strip&lpar;&rpar;

        &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; cousine &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; cousines:

            cousines[cousine] += &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;

        &lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:

            cousines[cousine] = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;

&lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; value &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;cousines&quot;&lt;/span&gt;]:

    cousines_handler&lpar;value&rpar;



print&lpar;cousines&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# convert this to dataframe&lt;/span&gt;
cousines = pd.DataFrame&lpar;list&lpar;cousines.items&lpar;&rpar;&rpar;, columns=[&lt;span class=&quot;hljs-string&quot;&gt;&quot;cousines&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;]&rpar;

cousines


&lt;span class=&quot;hljs-comment&quot;&gt;# getting the top 10 cousines&lt;/span&gt;
top_10_cousines = cousines.sort_values&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;, ascending=&lt;span class=&quot;hljs-literal&quot;&gt;False&lt;/span&gt;&rpar;.head&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# plotting the top 10 cousines&lt;/span&gt;
top_10_cousines_bar_plot = sns.barplot&lpar;data=top_10_cousines, x=&lt;span class=&quot;hljs-string&quot;&gt;&quot;cousines&quot;&lt;/span&gt;,y=&lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;&rpar;

top_10_cousines_bar_plot.set_xticklabels&lpar;top_10_cousines_bar_plot.get_xticklabels&lpar;&rpar;, rotation=&lt;span class=&quot;hljs-number&quot;&gt;45&lt;/span&gt;, horizontalalignment=&lt;span class=&quot;hljs-string&quot;&gt;&#39;right&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here, first, we are creating a dictionary that will hold the count for every cuisine.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then, the function &lt;code&gt;cousines_handler&lpar;&rpar;&lt;/code&gt; is used to fill the dictionary&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, we converted the dictionary into a data frame just for best practices otherwise you could directly find the top 10 cuisines from the dictionary too.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, we sorted the data frame in a decreasing manner using the &lt;code&gt;count&lt;/code&gt; column.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, we plotted a bar graph with the above data and the last line is used to make the x-ticks rotate to 45 degrees so that the labels are easily visible.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078601360/f91aa8e8-0d28-42b7-aada-6ecb5bba1301.png&quot; alt=&quot;Top 10 Cuisines Served&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;You can observe that the most served cuisine is North Indian followed by Chinese.&lt;/p&gt;
&lt;h3 id=&quot;heading-top-10-locations-with-highest-restaurants&quot;&gt;Top 10 Locations with Highest Restaurants&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# top 10 locations with highest restaurants&lt;/span&gt;

number_of_outlets = df.groupby&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;location&quot;&lt;/span&gt;&rpar;[&lt;span class=&quot;hljs-string&quot;&gt;&quot;name&quot;&lt;/span&gt;].count&lpar;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# getting the top 10 location with most number of restaurants&lt;/span&gt;
top_10_location_with_highest_restaurants = number_of_outlets.sort_values&lpar;ascending=&lt;span class=&quot;hljs-literal&quot;&gt;False&lt;/span&gt;&rpar;.head&lpar;&lt;span class=&quot;hljs-number&quot;&gt;10&lt;/span&gt;&rpar;


&lt;span class=&quot;hljs-comment&quot;&gt;# plotting the top 10 locations&lt;/span&gt;
top_10_location_with_highest_restaurants_bar_plot = sns.barplot&lpar;x=top_10_location_with_highest_restaurants.index, y=top_10_location_with_highest_restaurants.values&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# setting the xticks&lt;/span&gt;
top_10_location_with_highest_restaurants_bar_plot.set_xticklabels&lpar;top_10_location_with_highest_restaurants_bar_plot.get_xticklabels&lpar;&rpar;, rotation=&lt;span class=&quot;hljs-number&quot;&gt;45&lt;/span&gt;, horizontalalignment=&lt;span class=&quot;hljs-string&quot;&gt;&#39;right&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;Here we are grouping the data using location.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then count the number of restaurants per location using the name.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, we just sort the restaurants in a decreasing manner concerning count and retrieving the top 10 using &lt;code&gt;head&lpar;10&rpar;&lt;/code&gt;.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Now, just plot the above result using seaborn, this is very similar to the top 10 cuisine question.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078705916/c07e003c-2f1e-4009-9226-8a4e7a45c98e.png&quot; alt=&quot;Top 10 Locations with Highest Restaurants&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;From this, we can observe that BTM has the most number of restaurants.&lt;/p&gt;
&lt;h3 id=&quot;heading-top-10-liked-dishes&quot;&gt;Top 10 Liked Dishes&lt;/h3&gt;
&lt;pre&gt;&lt;code class=&quot;lang-python&quot;&gt;&lt;span class=&quot;hljs-comment&quot;&gt;# top 10 liked dishes&lt;/span&gt;

liked_dishes = {}

&lt;span class=&quot;hljs-function&quot;&gt;&lt;span class=&quot;hljs-keyword&quot;&gt;def&lt;/span&gt; &lt;span class=&quot;hljs-title&quot;&gt;liked_dishes_handler&lt;/span&gt;&lpar;&lt;span class=&quot;hljs-params&quot;&gt;value&lt;/span&gt;&rpar;:&lt;/span&gt;

    value = str&lpar;value&rpar;.split&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&#39;,&#39;&lt;/span&gt;&rpar;

    &lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; liked_dish &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; value:

        liked_dish = liked_dish.strip&lpar;&rpar;

        &lt;span class=&quot;hljs-keyword&quot;&gt;if&lt;/span&gt; liked_dish &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; liked_dishes:

            liked_dishes[liked_dish] += &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;

        &lt;span class=&quot;hljs-keyword&quot;&gt;else&lt;/span&gt;:

            liked_dishes[liked_dish] = &lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;

&lt;span class=&quot;hljs-keyword&quot;&gt;for&lt;/span&gt; value &lt;span class=&quot;hljs-keyword&quot;&gt;in&lt;/span&gt; df[&lt;span class=&quot;hljs-string&quot;&gt;&quot;dish_liked&quot;&lt;/span&gt;]:

    liked_dishes_handler&lpar;value&rpar;



print&lpar;liked_dishes&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# convert this to dataframe&lt;/span&gt;

liked_dishes = pd.DataFrame&lpar;list&lpar;liked_dishes.items&lpar;&rpar;&rpar;, columns=[&lt;span class=&quot;hljs-string&quot;&gt;&quot;dishes&quot;&lt;/span&gt;, &lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;]&rpar;

liked_dishes


&lt;span class=&quot;hljs-comment&quot;&gt;# getting the top 10 liked dishes&lt;/span&gt;
top_10_liked_dishes = liked_dishes.sort_values&lpar;&lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;, ascending=&lt;span class=&quot;hljs-literal&quot;&gt;False&lt;/span&gt;&rpar;[&lt;span class=&quot;hljs-number&quot;&gt;1&lt;/span&gt;:&lt;span class=&quot;hljs-number&quot;&gt;11&lt;/span&gt;]


&lt;span class=&quot;hljs-comment&quot;&gt;# plotting the top 10 dishes&lt;/span&gt;
top_10_liked_dishes_bar_plot = sns.barplot&lpar;data=top_10_liked_dishes, x=&lt;span class=&quot;hljs-string&quot;&gt;&quot;dishes&quot;&lt;/span&gt;,y=&lt;span class=&quot;hljs-string&quot;&gt;&quot;count&quot;&lt;/span&gt;&rpar;

&lt;span class=&quot;hljs-comment&quot;&gt;# setting the x-ticks&lt;/span&gt;
top_10_liked_dishes_bar_plot.set_xticklabels&lpar;top_10_liked_dishes_bar_plot.get_xticklabels&lpar;&rpar;, rotation=&lt;span class=&quot;hljs-number&quot;&gt;45&lt;/span&gt;, horizontalalignment=&lt;span class=&quot;hljs-string&quot;&gt;&#39;right&#39;&lt;/span&gt;&rpar;
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;We are handling this almost the same as we did with the top 10 cuisine questions:&lt;/p&gt;
&lt;ul&gt;
&lt;li&gt;&lt;p&gt;We created a dictionary to store the count of liked_dish per dish.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Then the function is used to fill the dictionary with the dish as key and count as value.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;We converted the dictionary to a data frame.&lt;/p&gt;
&lt;/li&gt;
&lt;li&gt;&lt;p&gt;Finally, we sorted the data frame in decreasing order concerning count and plotted it using a barplot.&lt;/p&gt;
&lt;/li&gt;
&lt;/ul&gt;
&lt;p&gt;&lt;img src=&quot;https://cdn.hashnode.com/res/hashnode/image/upload/v1682078789374/91e52152-a1cc-4d6e-95cd-1742d24e2ef4.png&quot; alt=&quot;top 10 liked dishes&quot; class=&quot;image--center mx-auto&quot; /&gt;&lt;/p&gt;
&lt;p&gt;From this, we can observe that Pasta is the most liked dish followed by Burgers.&lt;/p&gt;
&lt;h1 id=&quot;heading-conclusion&quot;&gt;Conclusion&lt;/h1&gt;
&lt;p&gt;Based on the exploratory data analysis &lpar;EDA&rpar; conducted on the Zomato dataset, several insights have been uncovered about the food industry and consumer preferences in different cities across India.&lt;/p&gt;
&lt;p&gt;The analysis revealed that online ordering and delivery have become increasingly popular, especially in urban areas. This trend has been further accelerated by the COVID-19 pandemic, which has led to a shift toward contactless and online ordering options.&lt;/p&gt;
&lt;p&gt;One of the key findings of the analysis was the popularity of North Indian cuisine across most cities, followed by Chinese and South Indian cuisine. This highlights the importance of understanding regional food preferences to cater to the local market.&lt;/p&gt;
&lt;p&gt;Another significant insight has been found that pasta is the most popular dish among consumers, followed by burgers. These insights can be used by food businesses to better understand consumer preferences and cater to their needs to improve customer satisfaction and drive business growth.&lt;/p&gt;
&lt;p&gt;Overall, the EDA on the Zomato dataset provides valuable insights into the food industry and consumer behavior in India. These insights can be leveraged by businesses and policymakers to make data-driven decisions and improve their understanding of the market.&lt;/p&gt;
<!-- BLOGPOSTS:END -->

<!--
**dotslashbit/dotslashbit** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
