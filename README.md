//# RUNLENGTH-PROGRAMM
package COM.RAUDRA;

public class RunLength
{
    public String encoder(String touncode)
    {
        int counter=1 ;
        StringBuilder encodedString=new StringBuilder();
        for(int i=1;i<=touncode.length();i++)
        {
             if (i==touncode.length()||touncode.charAt(i)!=touncode.charAt(i-1))
             {
                 encodedString.append(counter);
                 encodedString.append(touncode.charAt(i-1));
                 counter=1;
             }
             else
             {
                 counter++;
             }
        }
        return encodedString.toString();
    }

    public static void main(String[] args)
    {
        String testcase="aaaaabbbbbcccc";
        RunLength object=new RunLength();
        System.out.println(object.encoder(testcase));
    }
}
