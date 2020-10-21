# 实验报告

# 实验要求：
完成教材p110 第四题关于PC、内存等模拟的程序。
附加要求：
类中定义不少于两个构造方法；
每个类定义不少于2个属性，且属性的类型应该多样化；
根据课堂中关于访问权限的内容，尝试定义属性的修饰符多样化，类中定义方法操作属性，避免直接通过“类对象.属性”的形式访问属性值；且定义的方法内应该有符合常理的逻辑判断；
尝试把本次实验的多个类放置在不同的包中，体会修饰符private的用法。
用类描述计算机中 CPU 的速度和硬盘的容量
本项目涉及四个类分别是CPU类、HardDisk类、PC类、Test类用来展示
# 实验设计
1.class CPU
  类的定义：
package packet4;


public class CPU{  //cpu 类
private int speed;
private String name;
public CPU(int spd,String nm){
	this.speed=spd;
	this.name=nm;
}  //空构造方法
public CPU(int spd){
    	this.speed=spd;
    	this.name="";
    }
public CPU(){
	
}  //空构造方法
public int getSpeed(){
return speed;
}
public void setSpeed(int m){
speed=m;
}
}

2.HardDisk类
 package packet3;

public class HardDisk{
	private int amount;
	private String name;
public HardDisk(int amt,String nm){
	this.name=nm;
	this.amount=amt;
	
}  //空构造方法
public HardDisk(){
	
}  
public HardDisk(int amt){
    	this.amount=amt;
    	this.name="";
    }

public int getAmount(){
return amount;
}
public void setAmount(int m){
amount=m;
}
}

3.PC 类
package packet2;

import packet4.CPU;
import packet3.HardDisk;


public class PC{
	private HardDisk HD;
	private CPU cpu;

public PC(){
	
}  //空构造方法
public PC(HardDisk hd,CPU cu){
   	this.HD=hd;
   	this.cpu=cu;
   }
public void setCPU(CPU c){
cpu=c;
}
public void setHardDisk(HardDisk h){
HD=h;
}
public void show(){
System.out.println("CPU的速度是"+cpu.getSpeed());
System.out.println("硬盘的容量是"+HD.getAmount());
}
}

4.Test类
package test;
import packet2.PC;
import packet3.HardDisk;
import packet4.CPU;

 
public class Test{
public static void main(String args[]){
CPU cpu=new CPU();
HardDisk disk=new HardDisk();
cpu.setSpeed(2200);
disk.setAmount(200);
PC pc=new PC();
pc.setCPU(cpu);
pc.setHardDisk(disk);
pc.show();
}
}

# 实验思路
Test类中包含main方法，通过将cpu速度speed设置为 2200，将硬盘的amount设置为200，然后通过调用pc的show()方法，展示cpu速度和硬盘信息


实验感悟：挺难的，以后得多下功夫
