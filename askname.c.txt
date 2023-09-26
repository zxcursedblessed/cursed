/* askname.c */
#include &lt;stdio.h&gt;
#include &lt;string.h&gt;
void askname(char *first, char *last)
{
printf(&quot;Enter your first name: &quot;);
fgets(first, 255, stdin);
first[strlen(first)-1] = &#39;\0&#39;; /* remove the newline at the end */
printf(&quot;Now enter your last name: &quot;);
gets(last); /* buffer overflow? what&#39;s that? */
}