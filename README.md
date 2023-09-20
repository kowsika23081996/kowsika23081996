/*<applet code="Drawshape.class" width=500 height=500> </applet>*/

import java.awt.*;

import java.awt.event.*;

import java.applet.*;

public class Drawshape extends Applet implements MouseListener

{

int X,Y,ch;

public void init()

{

addMouseListener(this);

ch=1;

}

public void paint(Graphics g)

{

switch(ch)

{

case 1:

g.drawOval(X,Y,50,50);

break;

case 2:

g.drawRect(X,Y,60,50);

break;

case 3:

g.drawOval(X,Y,200,250);

break;

case 4:

g.drawRect(X,Y,250,100);

break;

}

ch++;
if(ch==5)
{
ch=1;
}
showStatus(X+","+Y);
}
public void mouseClicked(MouseEvent me)
{
X=me.getX();
Y=me.getY();
repaint();
}
public void mouseEntered(MouseEvent me)
{
X=me.getX();
Y=me.getY();
repaint();
}
public void mouseExited(MouseEvent me) { }
public void mousePressed(MouseEvent me) { }
public void mouseDragged(MouseEvent me) { }
public void mouseReleased(MouseEvent me) { }
}


<!---
kowsika23081996/kowsika23081996 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
