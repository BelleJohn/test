# test
 
 
function output=Kernel_fun(x1,x2,sigma)
[x1_trial ~]=size(x1);
[x2_trial ~]=size(x2);
output=zeros(x1_trial,x2_trial);
for i =1:x1_trial
    for j=1:x2_trial
        kernel=exp( -1*((x1(i,:)-x2(j,:))*transpose(x1(i,:)-x2(j,:))) / (2*sigma^2) );
        output(i,j)=kernel;
    end
end
