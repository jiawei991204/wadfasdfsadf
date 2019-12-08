实验学生选课系统设计
========
#实验目的
<br>分析学生选课系统
使用GUI窗体及其组件设计窗体界面
完成学生选课过程业务逻辑编程
基于文件保存并读取数据
处理异常<br>
#实验要求
<br>
1、设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
2、基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
3、针对操作过程中可能会出现的各种异常，做异常处理
4、基于输入/输出编程，支持学生、课程、教师等数据的读写操作。
5、基于Github.com提交实验，包括实验SRC源文件夹程序、README.MD实验报告文档。
6、本次实验是综合性实验，在40%的实验成绩中占比最大，望同学们认真对待。
<br>

#流程图
![image](https://github.com/jiawei991204/wadfasdfsadf/blob/master/890560093569985364.png)\
#实验过程：
<br> 运用gui，数组的添加删除，文件操作，输入输出以及异常处理进行编辑
#核心代码：
<br>package GUI;
import javax.swing.JLabel;
import java.awt.Font;

import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JDialog;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import javax.swing.JList;
import java.awt.BorderLayout;
import java.awt.FlowLayout;
import javax.swing.DefaultListModel;
import javax.swing.JButton;
	public print() {
		setTitle("Print Classes");
		setBounds(200, 200, 700, 400);
		getContentPane().setLayout(new BorderLayout());
		contentPanel.setLayout(new FlowLayout());
		contentPanel.setBorder(new EmptyBorder(20, 20, 20, 20));
		getContentPane().add(contentPanel, BorderLayout.CENTER);
		{   	try {
			BufferedReader brs = new BufferedReader(new FileReader("C:\\Users\\Desktop\\Java\\Java实验\\numbers.txt"));
            String Student_num = brs.readLine();
            brs.close();
	        BufferedReader br = new BufferedReader(new FileReader("C:\\Users\\Desktop\\Java\\Java实验\\" + Student_num +".txt"));
	        String demo = br.readLine();
       	    br.close();
	        JLabel lblNewLabel = new JLabel("You have chosen classes below:");
			lblNewLabel.setFont(new Font("微软雅黑", Font.BOLD | Font.ITALIC, 14));
			contentPanel.add(lblNewLabel);
	        {   
	        	DefaultListModel listModel=new DefaultListModel(); 
	        	JList list = new JList(listModel);
	        	contentPanel.add(list);
	             String [] demoarray = demo.split(";");
	             for (int i=0; i<demoarray.length ;i++) {
	         		listModel.addElement(demoarray[i]);
	             }
	        }
	    } catch (IOException e1) {
	        e1.printStackTrace();
	    }
		}
		{
			JPanel buttonPane = new JPanel();
			buttonPane.setLayout(new FlowLayout(FlowLayout.RIGHT));
			getContentPane().add(buttonPane, BorderLayout.SOUTH);
			{
				JButton okButton = new JButton("OK");
				okButton.setActionCommand("OK");
				buttonPane.add(okButton);
				getRootPane().setDefaultButton(okButton);\<br>
#实验截图
![image](https://github.com/jiawei991204/wadfasdfsadf/blob/master/901873982620321021.jpg)\
#实验心得
<br>这次将之前所有的实验进行了结合，有了一套完整一些的系统，学会了分析学生选课系统使用，运用了列表数组的添加，GUI窗体及其组件设计窗体界面，
完成学生选课过程业务逻辑编程，基于文件保存并读取数据，也进行了异常处理
<br>
