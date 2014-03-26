---
layout: post
title: "==与isEqual区别"
date: 2014-03-26 14:43:54 +0800
comments: true
categories: 
---

-  == 主要是比较两个内存地址是否相同。  
-  isEqual 是比较两个数据对应[哈希值](http://www.baike.com/wiki/%E5%93%88%E5%B8%8C%E5%80%BC)是否相同。  
-  isEqual 首先判断两个对象是否类型一致，接着判断具体内容是否一致，如果类型不同直接return no。
 

- 通过NSString来比较这个问题  

		NSString *string1 = @"111";
		NSString *string2 = @"111";  
		
		打印内存地址
		NSLog@("string1 = %p, string2 = %p", string1, string2);
		string1 = 0xdd4ec, string2 = 0xdd4ec  
		所以 if (string1 == string2) return YES;  
		
		打印hash值  
		NSLog(@"hash stinrg1 = %d, string2 = %d ", [string1 hash], [string2 hash]);  
		hash string1 = 487555398, string2 = 487555398;
  		
        所以 if ([string1 isEqual:string2]) return YES;
        
        --------------------------------------------------------------------------
        
        NSString *str1 = [[NSString alloc]initWithFormat:@"111"];  
        NSString *str2 = [[NSString alloc]initWithFormat:@"111"];
		
		打印内存地址  
		NSLog(@"内存  str1 = %p ,str2 = %p",str1,str2);
		内存 str1 = 0x1d888520 ,str2 = 0x1d888530
		所以 if (str1 == str2) return NO;
		
		打印hash值  
		NSLog(@"hash str1 = %d ,str2 = %d",[str1 hash],[str2 hash]);  
		hash str1 = 487555398 ,str2 = 487555398
		所以 if ([str1 isEqual:str2]) return YES;

- 通过UIImage来比较
		
		UIImage* img1=[UIImage imageNamed:@"image.png"];  
		UIImage* img2=[UIImage imageNamed:@"image.png"];  
		
		打印内存地址  
		NSLog(@"img1 = %p , img2 = %p",img1,img2);		img1 = 0x1cd76320 , img2 = 0x1cd76320
		所以 if(img1 == img2) return YES;  
		
		打印hash值  
		NSLog(@"hash img1 = %d , img2 = %d",[img1 hash],[img2 hash]);  
		hash img1 = 483877664 , img2 = 483877664;  
		所以 if([img1 isEqual:img2]) return YES;
		
- 综上: == 相同时hash值一定相同， hash相同是 == 不一定相等。  


  
  
  
  
  
  
  		
	
	
	
	
 	
