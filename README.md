# Practice

public class CodeWordChecker implements StringChecker
{
  private int minLength;
  private int maxLength;
  private String notValid;
  
  public CodeWordChecker(int min, int max, String s)
  {
    minLength = min;
    maxLength = max;
    notValid = s;
  }
  
  public CodeWordChecker(String s)
  {
    minLength = 6;
    maxLength = 20;
    notValid = s;
  }
  
  public boolean isValid(String str)
  {
    return (str.length()>=minLength && str.length()<=maxLength)&& str.indexOf(notValid)==-1;
  }
}
