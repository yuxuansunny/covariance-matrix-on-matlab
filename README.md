# covariance-matrix-on-matlab
Matlab realization on covariance matrix
>> Mysample=fix(rand(10,3)*50)

Mysample =

    40     7    32
    45    48     1
     6    47    42
    45    24    46
    31    40    33
     4     7    37
    13    21    37
    27    45    19
    47    39    32
    48    47     8

>> dim1=Mysample(:,1);
>> dim2=Mysample(:,2);
>> dim3=Mysample(:,3);
>> cov12=sum((dim1-mean(dim1)).*(dim2-mean(dim2)))/(size(Mysample,1)-1);
>> cov13=sum((dim1-mean(dim1)).*(dim3-mean(dim3)))/(size(Mysample,1)-1);
>> cov23=sum((dim2-mean(dim2)).*(dim3-mean(dim3)))/(size(Mysample,1)-1);
>> var1=std(dim1)^2;
>> var2=std(dim2)^2;
>> var3=std(dim3)^2;
>> cov(Mysample)

ans =

  301.1556   78.0000 -120.2444
   78.0000  268.9444 -126.9444
 -120.2444 -126.9444  216.0111
