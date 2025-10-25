---
layout: post
title: Automotive-SW-testing
---

Automotive SW testing?

<p align="center">
<img src="/images/test.gif" width="450">
</p>


**the process of verifying and validating a vehicle's software to ensure it functions correctly, safely, and reliably, especially for safety-critical systems like braking and steering.** This includes various tests like functional, structural coverage, and worst-case execution time analysis, and is guided by industry standards such as ISO 26262 (for functional safety), MISRA (for coding standards), and AUTOSAR (for embedded software). Testing also increasingly includes cybersecurity testing due to the connected nature of modern cars. 


#### Industry standards:
- ISO 26262: A standard for functional safety in road vehicles, guiding risk-based development of safety-critical software. 
- MISRA C: Provides coding guidelines to improve the safety and security of C/C++ software used in automotive systems. 
- AUTOSAR: Defines a standard architecture for the development of embedded software for electronic control units (ECUs). 
- ASPICE (automotive software process improvement capability determination): To improve the quality and sophistication of software and embedded systems development processes. 
<p align="center">
<img src="/images/ASPICE4.png" width="450">
</p>


####  Testing levels
Tests are performed at different levels, including:
- Software Unit Verification
- Software Integration and Integration Test
- Software Qualification Test
- System Integration and Integration Test
- System Qualification Test 



-----------------------------------------------------------------------


### V&V (Verification & Validation)

Verification and validation (also abbreviated as V&V) are independent procedures that are used together for checking that a product, service, or system meets requirements and specifications and that it fulfills its intended purpose.These are critical components of a quality management system such as ISO 9000. The words "verification" and "validation" are sometimes preceded with "independent", indicating that the verification and validation is to be performed by a disinterested third party. "Independent verification and validation" can be abbreviated as "IV&V".

<p align="center">
<img src="/images/V model.png" width="450">
</p>

### TDD test 
In the context of V&V (Verification and Validation), TDD (Test-Driven Development) primarily falls under the Verification stage
TDD is based on writing automated **unit tests**. These tests constantly verify that each small unit of code behaves exactly as specified, ensuring the software is being built correctly at the lowest level.

Try TDD test on [cyber dojo](https://beta.cyber-dojo.org/creator/home)

<p align="center">
<img src="/images/01_TDDtest.png" width="450">
</p>

select your excercise, I choose **Fizz Buzz**

<p align="center">
<img src="/images/02_TDDtest.png" width="450">
</p>

choose language and test-framework 


<p align="center">
<img src="/images/03_TDDtest.png" width="450">
</p>

choose practice type, ensemble or classroom or solo. I select **solo**.

<p align="center">
<img src="/images/04_TDDtest.png" width="450">
</p>

Then, automaticallty ID is generated. If you want to check my practice, you can use my ID **PZvHpq** and check it anytime. 

<p align="center">
<img src="/images/05_TDDtest.png" width="450">
</p>

<p align="center">
<img src="/images/06_TDDtest.png" width="450">
</p>

add new TEST function

<p align="center">
<img src="/images/07_TDDtest.png" width="450">
</p>


test it, but get the error msg

<p align="center">
<img src="/images/08_TDDtest.png" width="450">
</p>

update **hiker.c** and **hiker.h** as below:

<p align="center">
<img src="/images/09_TDDtest.png" width="450">
</p>

<p align="center">
<img src="/images/10_TDDtest.png" width="450">
</p>

Test it again. But still get the error msg. why?

<p align="center">
<img src="/images/11_TDDtest.png" width="450">
</p>

Thus, fix **hiker.c**.

**previous version**
```
int answer()
{
    return 6 * 9
}
```

**updated version**
<p align="center">
<img src="/images/12_TDDtest.png" width="450">
</p>

Test again and not work well. 
<p align="center">
<img src="/images/13_TDDtest.png" width="450">
</p>

do refactoring as below:

- initialize **result**
- consider different variable name **intputNumber** instead of **i**

<p align="center">
<img src="/images/14_TDDtest.png" width="450">
</p>

Test it again

<p align="center">
<img src="/images/15_TDDtest.png" width="450">
</p>

Finally, check the **GCC code coverage Report** which is automatically generated. 

<p align="center">
<img src="/images/16_TDDtest.png" width="450">
</p>

You can check it by yourself using the attached file, **cyber-dojo-2025-10-25-PZvHpq.tgz**



🦦 Thanks for reading. Hope to see you again!


-----------------------------------------------------------------------

### Reference
- [Automotive SW test](google)
- [VV test](https://software-testing-tutorials-automation.com/2016/06/v-model-verification-and-validation.html)
- [Verification & Validation](https://en.wikipedia.org/wiki/Verification_and_validation)
- [ASPICE 4.0](https://rapidauto.io/%EC%9E%90%EB%8F%99%EC%B0%A8_%EC%82%B0%EC%97%85_%ED%91%9C%EC%A4%80/A-SPICE_%28%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4_%ED%8F%89%EA%B0%80_%ED%94%84%EB%A0%88%EC%9E%84%EC%9B%8C%ED%81%AC%29)