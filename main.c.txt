#include &lt;stdio.h&gt;
#include &lt;string.h&gt;
int main(int argc, char **argv)
{
char first[255], last[255];
printf(&quot;Enter your first name: &quot;);
fgets(first, 255, stdin);
first[strlen(first)-1] = &#39;\0&#39;; /* remove the newline at the end */
printf(&quot;Now enter your last name: &quot;);
gets(last); /* buffer overflow? what&#39;s that? */
printf(&quot;Hello %s %s!\n&quot;, first, last);
return 0;
}