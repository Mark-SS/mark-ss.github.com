---
layout: post
title: "第三方类库"
date: 2014-03-13 10:29:00 +0800
comments: true
categories: 
---

[LBBLurredImage](https://github.com/lukabernardi/LBBlurredImage) 是一个继承子UIImageView，轻而易举使图片模糊的项目。你将仅仅用一行海马来创建一个神奇的模糊效果。<center>![](https://raw.github.com/lukabernardi/LBBlurredImage/master/Resources/SimulatorScreenshot.png)</center>



[UILabel+ContentSize](https://gist.github.com/billyohgren/7944887)在UILabel内计算内容的大小。 

*UILabel+ContentSize.h*
	
	#import <UIKit/UIkit.h>
	
	@interface UILabel (ContentSize)
	
	- (CGSize)contentSize;
	
	@end
	
*UILabel+ContentSize.m*

	#import "UILabel+ContentSize.h"
	
	@implementation UILabel (ContentSize)
	
	- (CGSize)contentsize {
		NSMutableParagraphStyle *paragraphStyle = [[NSMutableParagraphStyle alloc] init];
	    paragraphStyle.lineBreakMode = self.lineBreakMode;
	    paragraphStyle.alignment = self.textAlignment;
	    NSDictionary * attributes = @{NSFontAttributeName : self.font,
	    							   NSParagraphStyleAttributeName : paragraphStyle};
	    							    CGSize contentSize = [self.text 
	    							    boundingRectWithSize:self.frame.size
                                                    options:(NSStringDrawingUsesLineFragmentOrigin|NSStringDrawingUsesFontLeading)
                                           attributes:attributes
                                              context:nil].size;
   		 return contentSize;
	}

  
