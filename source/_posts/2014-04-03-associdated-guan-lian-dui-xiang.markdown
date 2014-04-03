---
layout: post
title: "associdated 关联对象"
date: 2014-04-03 16:02:27 +0800
comments: true
categories: 
---
- 给已有的类有类别（category）的方式扩展属性。知道类别的一个关键的事实是，它是不能够包括属性和成员变量的。但是可以通过 <objc/runtime.h>中的函数关联属性。  
- 例如我们一个UIViewController的类别。  
		
		#import <UIKit/UIkit.h>
		
		@interface UIViewController (YCCommon)
		
		@propery (nonatomic, strong) id associdatedObject;
		
		@end
		
		----------------------------------------------------------------------------
		
		#import <UIViewController+YCCommon>  
		#import <objc/runtime.h>
		
		@implementation UIViewController (YCCommon)
		
		@dynamic associdatedObject;
		
		- (void)setAssocidatedObject:(id)object {  
			objc_setAssociatedObject(self, @selector(associdatedObject), object, OBJC_ASSOCIATION_RETAIN_NONATOMIC);
		}
		
		- (id)associdatedObject {  
			objc_getAssociatedObject(self, @selector(associdatedObject));
		}
		
		
		@end
		
		//通常用static char key来标识属性最好 更简单的方式实现： 用上面的 selector
		
		static const void *kAssocitaedObjectKey = &kAssocitaedObjectKey;
		
		- (void)setAssocidatedObject:(id)object {  
			objc_setAssociatedObject(self, kAssocitaedObjectKey, object, OBJC_ASSOCIATION_RETAIN_NONATOMIC);
		}
		
		- (id)associdatedObject {  
			objc_getAssociatedObject(self, kAssocitaedObjectKey);
		}
		
- <objc/runtime.h> 函数主要有 
- 、 OBJC_EXPORT void `objc_setAssociatedObject(id object, const void *key, id value, objc_AssociationPolicy policy)`
- OBJC_EXPORT id `objc_getAssociatedObject(id object, const void *key)`
- OBJC_EXPORT void `objc_removeAssociatedObjects(id object)`  
 
- 类别是扩展内核类，使用关联对象可以解决动态属性扩展实现。

更多参考可以看 [NSHipster](http://nshipster.cn/associated-objects)

