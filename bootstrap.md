###栅格源码分析
    1.流体容器&固体容器 公共样式
      margin-right:auto;
      margin-left:auto;
      padding-left: 15px;
      padding-right: 15px;
    
    2.固定容器 特定央视
      顺序不可变
        @media(min-width:@screen-sm-min){
          width:@container-sm;
        }
        @media(min-width:@screen-md-min){
          width:@container-md;
        }
        @media(min-width:@screen-lg-min){
          width:@container-lg;
        }
    3.行
      margin-left: -15px;
      margin-right: -15px;
    4.列
      .make-grid-columns()--->
        .col-xs-1, .col-sm-1, .col-md-1, .col-lg-1,
        ...
        
        .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12,{
          position: relative;
          min-height:1px;
          padding-left:15px;
          padding-right: 15px;
          }

      .make-grid(xs)--->
          float-grid-columns

###响应式工具
###栅格和模型设计
  容器两边具有15px的padding
  行  两边具有-15px的margin
  列  两边具有15px的padding

  为了维护槽宽的规则，
      列两边必须要有15px的padding
  为了能使列嵌套行，
      2.
  为了让容器可以包裹住行
      3。