
# Xiaomi Bootloader Unlock Code Variant Generator

## 理论依据
本工具的思想源自 **RSA 三老 1978 年的原始论文**：
> *A Method for Obtaining Digital Signatures and Public-Key Cryptosystems* (Communications of the ACM, Vol. 21, No. 2, Feb 1978)

论文明确定义了签名验证的本质：只要满足 `M ≡ S^e mod n`，签名即为合法，**不存在“唯一 S”或“范围校验”的数学约束**。
本工具正是利用这一底层性质，对已授权的解锁码进行同余变换（`S' = S + k*N`），生成无限个可通过公验的等价解锁码。

> 注意：本项目仅为学术研究用途，请勿用于非法用途。

About This Tool
 
This tool is used to generate many valid bootloader unlock codes for Xiaomi devices.
All you need is one original valid unlock code S.
From that single S, you can create as many valid unlock codes as you want.
These new codes all work normally, just like the original one.
This project is only for research and learning, not for illegal use.
 
How It Works
 
The principle comes from a mathematical property of the RSA encryption system.
 
The formula is:
S' = S + k × n
 
- S is your original valid unlock code
- n is a public number from Xiaomi’s bootloader public key
- k can be any integer, like 1, 2, 3, -1, -5
- S' is the new valid unlock code we generate
 
When the phone checks whether the unlock code is valid,
it only verifies the mathematical relationship.
So all S' generated this way will be recognized as legal and valid.
 
What This Tool Can Do
 
- Generate a large number of valid unlock codes from one original S
- Back up multiple usable unlock codes for future use
- Help researchers study how RSA works on Xiaomi phones
- Show a real example of RSA mathematical characteristics
 
What This Tool Cannot Do
 
- It cannot create a valid unlock code out of nowhere
- It cannot get Xiaomi’s private key
- It cannot bypass official unlock permissions
- It cannot help users who have no unlock eligibility at all
 
How to Use This Tool
 
1. Prepare your original valid unlock code S
2. Get the public modulus n from Xiaomi’s public key
3. Open the calculator inside 小米解锁码计算器.zip
4. Enter S, n, and any integer k
5. The tool will output a new valid unlock code S'
6. You can use this S' to unlock the device in fastboot mode
7. Change k to generate more valid unlock codes for backup
 
Community Research Challenge
 
I have provided the method to generate many valid unlock codes from one S.
Now the baton is passed to the whole community.
 
The next research goal is:
Can we find the original valid S using only public information?
Such as the device token, public key e, and public modulus n.
 
Everyone is welcome to study, test, and share discoveries together.
 
Disclaimer
 
This project is for academic research and educational purposes only.
Unauthorized bootloader unlocking may void your device warranty.
The author is not responsible for any risks, losses, or legal problems caused by misuse.
Please abide by the laws and regulations of your region.
 
 
 
 
