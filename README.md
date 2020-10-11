# 实验报告
用类描述计算机中 CPU 的速度和硬盘的容量
本项目涉及四个类分别是CPU类、HardDisk类、PC类、Test类用来展示
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

Test类中包含main方法，通过将cpu速度speed设置为 2200，将硬盘的amount设置为200，然后通过调用pc的show()方法，展示cpu速度和硬盘信息



