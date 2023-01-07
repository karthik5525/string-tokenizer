# string-tokenizer



import java.util.*;

class First

{synchronized public void display(String msg)

{System.out.println("[" + msg);

try

  {Thread.sleep(1000);

  }

catch(InterruptedException e)

  {e.printStackTrace();

  }

System.out.println("]");

}

}

class second extends Thread

{String msg;

First fobj;

second(First fp,String str)

  {fobj=fp;

  msg=str;

  start();

  }

public void run()

  {fobj.display(msg);

  }

}

class threadsyncronization

{public static void main(String args[])

  {First fnew=new First();

  second ss=new second(fnew,"welcome");

  second ss1=new second(fnew,"new");

  second ss2=new second(fnew,"programmer");

  }

}
