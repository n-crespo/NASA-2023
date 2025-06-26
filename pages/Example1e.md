# Example1e

- describes existential version of Example 1a

  ```py
  iterated('R=="<{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0)");
  iterated('R=="x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>#<{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0)#");
  orR('R=="x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0))");
  iterated('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>#<{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0)#)");
  diamondOr('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0|#<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0))#)");
  diamondOr('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0))");
  orR('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0))");
  diamondOr('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0))");
  hideR('R=="x=E()&v=0");
  hideR('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)");
  orR('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0)");
  hideR('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}}*>(x=E()&v=0)");
  choiced('R=="<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)");
  choiced('R=="<{x'=v,v'=a&x<=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>#<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)#");
  orR('R=="<{x'=v,v'=a&x<=bf()}><{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(<{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0))");
  composed('R=="<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(<{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0))");
  hideR('R=="<?x=bf();vi:=v;><{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(<{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0))");
  choiced('R=="<{x'=v,v'=a&x<=bf()}>#<{x'=v,v'=a&x<=bf()}++{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)#");
  solve('R=="<{x'=v,v'=a&x<=bf()}>(<{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0))");
  existsR("(sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a", 'R=="\exists t_ (t_>=0&\forall s_ (0<=s_&s_<=t_->a*(s_^2/2)+v_1*s_+x_1<=bf())&\forall v (v=a*t_+v_1->\forall x (x=a*(t_^2/2)+v_1*t_+x_1-><{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0))))");
  andR('R=="(sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a>=0&\forall s_ (0<=s_&s_<=(sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a->a*(s_^2/2)+v_1*s_+x_1<=bf())&\forall v (v=a*((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)+v_1->\forall x (x=a*(((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)^2/2)+v_1*((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)+x_1-><{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)))"); <(
    "(sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a>=0":
      todo,
    "\forall s_ (0<=s_&s_<=(sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a->a*(s_^2/2)+v_1*s_+x_1<=bf())&\forall v (v=a*((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)+v_1->\forall x (x=a*(((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)^2/2)+v_1*((sqrt(4*a*bf()-4*a*x_1+v_1^2)-v_1)/2*a)+x_1-><{x'=v,v'=a&x<=bf()}>(x=E()&v=0)|<{?x=bf();vi:=v;}{x'=v,v'=-vi^2/(2*(E()-bf()))&x>=bf()}>(x=E()&v=0)))":
      todo
  )
  ```
