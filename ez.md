## EZ
>Sol:
It exe asks for the password, 2 functions change the value.. and check with a hardcoded string.
Opened in ghidra
```c
  int main(int _Argc,char **_Argv,char **_Env)

{
  int iVar1;
  longlong lVar2;
  char *pcVar3;
  undefined4 in_register_0000000c;
  char local_1c8 [112];
  char local_158 [112];
  char local_e8 [112];
  char local_78 [112];
  
  __main(CONCAT44(in_register_0000000c,_Argc));
  printf("Enter passcode :");
  lVar2 = __getreent();
  fgets(local_78,0x2a,*(FILE **)(lVar2 + 8));
  strcpy(local_1c8,local_78);
  lVar2 = solo((longlong)local_78);
  pcVar3 = (char *)lol(lVar2);
  strcpy(local_e8,pcVar3);
  iVar1 = strcmp(local_e8,"lcZdl_Yoati+Xjn,lN!gGRdNR-R]H`=XjN,lo*+Iv");
  if (iVar1 == 0) {
    pcVar3 = (char *)goodjob((longlong)local_1c8);
    strcpy(local_158,pcVar3);
    printf("Congrats!!  \nflag: %s\n",local_158);
  }
  else {
    puts("So sorry sister :(");
  }
  return 0;
}

```
Revesred the 2 functions and passed to the function that gives the flag.
>Script:
```py
check = "lcZdl_Yoati+Xjn,lN!gGRdNR-R]H`=XjN,lo*+Iv"

def check2_rev(s):
    s = list(s)
    for i in range(len(s)):
        if( i > 3 and i <= 6 ):
            s[i] = chr(ord(s[i])+3)
        elif( i > 29 or i <= 16 ):
            s[i] = chr(ord(s[i])-5)
        else:
            s[i] = chr(ord(s[i])^4)
    return s

def check1_rev(s):
    s = list(s)
    for i in range(len(s)):
        s[i] = chr((ord(s[i]) +5)^1)
    return s

def get_flag(s):
    s = list(s)
    for i in range(len(s)):
        if ( i <= 19 or i > 29 ):
            s[i] = chr(ord(s[i]) + 6)
        else:
            s[i] = chr(ord(s[i]) + 5)
    return s

flag = check1_rev(check2_rev(check))
flag2 = "".join(get_flag(flag))
print(flag2)
```