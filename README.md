# 22-23 spring Bioinfomatic course
> Beginning on 2023/2/23, it is a site of 22-23 spring Bioinfomatic course presented by 鲁志.   
陈韬衡 2020011582

# Content
1. [Lecture_1](#lecture-1) 
2. 


# Lecture 1 (2023/2/23)

## Learning materials
1. [tsinghua_cloud] (https://cloud.tsinghua.edu.cn/d/ad22768345664924b202/?p=%2FFiles&mode=list)   
2. [bioinfo_tutorial] (https://book.ncrnalab.org/teaching)   
3. [syllabus] (https://app.yinxiang.com/fx/48420550-8f51-49a6-b404-0cc7e810ab4c) 
4. [Linux_commands] (https://www.runoob.com/linux/linux-command-manual.html)

## Mark Down   
Learn its [grammar] (https://markdown.com.cn/).   

### What is gene?   
Gene is a sequence of information in the nucleotide. 

### Why genes are so few in humankind?  
The size of genome is not related to the evolution of creatures. It doesn't mean that superior creatures own more base-pair than the lower ones.   
Humankind owns about 3Gbp. However, 90 percent of them are not coding genes. The extra base-pairs are not useless. Several functions have been revealed in the resent a few decades. 

### What are the defferences between algorithm and model?    
算法不是我可以掌握的东西，模型不是我可理解的，但一定程度上我可以使用它。

### What problems is bioinformatics trying to solve? 

# lecture 4
BLAST
 
## what is BLAST?   
BLAST 通过评分表比对两个序列，正配、错配、空缺有不同的得分。最基本的BLAST通过积分表生成反应两个序列相似程度的一个矩阵。从矩阵主对角线的一角开始，寻找一条累加计分最高的路径。该得分越高说明相似程度（同源性）越高。然后返回来找到这条路径上的个点。   

## How to speed up BLAST? 
1. dynamic programming 
2. seeding and extanding. 
3. 屏蔽简单重复序列。

### seeding and extanding 
将query序列剪成固定长度的序列，（3 aa 或者 11 bp）。这些seed相互重叠，完全覆盖整个query序列。然后在数据库里面查找这些seed的位置。数据库经过预处理，以快速应对不同seed的查找。对所有seed进行查找后，可以生成query序列和各条候选序列的hit map。如果存在连续多个seed在候选序列中连续对应，hit map则会在相应位置上出现平行于主对角线的连续热点。针对这些热点区域两端扩展进行搜索，直至得分低于一个设定值。最后动态规划，对比。 


# end 

