<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 Pro (24H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 **Install Active Directory**
- Step 2 **Create a Domain Admin user within the domain**
- Step 3 **Join Client-1 to your domain**
- Step 4 **Setup Remote Desktop for non-administrative users on Client-1**
- Step 5 **Create addiotional users and attempt to log into Client-1 with one of the users**

<h2>Deployment and Configuration Steps</h2>


<p>

**Step 1-** **Install Active Directory / Log In**

</p>

Begin by selecting dc-1 from miscrosoft remote desktop↓ 

<p>
<img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/dddd7d60-b01f-4e4e-a321-0f5f49395254" />
<p>

Log into the Virtual Machine.↓

<p>
 Username: shylabuser 
</p>

<p>
 Password: Myworldlab123! 
</p>

<p>

**Click Continue**
 
</p>

<img width="435" height="224" alt="Azure step 31" src="https://github.com/user-attachments/assets/b56c67c2-5b4d-4af4-8c77-308f6f395b84" />
</p>

<p>

**Click Continue↓**

</p>


<img width="579" height="158" alt="Azure step 32" src="https://github.com/user-attachments/assets/28c32b2f-960c-4e03-8d91-e8ac9db078ad" />
<p>

<p>

**Click the start menu and go to Server Manager↓**
 
</p>

 
<img width="325" height="670" alt="Azure step 62" src="https://github.com/user-attachments/assets/4f8b080d-b7a0-4113-a145-a5ddb1f5f86d" />
</p>

<p>

**Click Add roles and features↓**
 
</p>


<img width="1073" height="353" alt="Azure step 63" src="https://github.com/user-attachments/assets/f5a4fbb2-ce1c-44b1-a21c-60ecf93c2f7f" />


<p>

**Click Next↓**
 
</p>


<img width="778" height="524" alt="Azure step 64" src="https://github.com/user-attachments/assets/5b0b00aa-e02e-4a98-81b3-da34d20c5824" />


<p>

**Click Next↓**
 
</p>

<img width="778" height="553" alt="Azure step 65" src="https://github.com/user-attachments/assets/e566bd89-6f07-4389-a953-87e927cf2c3b" />


<p>

**Click Next↓**
 
</p>


<img width="761" height="509" alt="Azure step 66" src="https://github.com/user-attachments/assets/fe88baaa-aeca-4f25-9c92-28108868301f" />

<p>

**Click Active Directory Domain Services↓**
 
</p>


<p>
<img width="337" height="183" alt="Azure step 67" src="https://github.com/user-attachments/assets/cc0b21f5-0cf7-4803-ae05-665815d9bafc" />
</p>

<p>

**Click Add Features↓**
 
</p>




<img width="415" height="436" alt="Azure step 68" src="https://github.com/user-attachments/assets/00a265b4-dbd4-4265-b10a-5fddb66a8217" />

<p>

**Check Mark next to Active Directory Domain Services and Click Next↓**
 
</p>


<p>
<img width="584" height="454" alt="Azure step 69" src="https://github.com/user-attachments/assets/f5ae9f12-4a29-4a20-a8df-109173eddb25" />
</p>

<p>

**Click Next↓**
 
</p>

<img width="585" height="427" alt="Azure step 70" src="https://github.com/user-attachments/assets/c8922291-6e86-4bc6-9cd8-1ed4242f93eb" />

<p>

**Click Next↓**
 
</p>




<img width="581" height="450" alt="Azure step 71" src="https://github.com/user-attachments/assets/be838879-4a81-445a-a64c-dca53e86104b" />

<p>

**Check Mark next to Restart the destination server automatically if required and Click "YES" to allow automatic restarts↓**
 
</p>


<img width="683" height="402" alt="Azure step 72" src="https://github.com/user-attachments/assets/fdffbb4d-30d2-4b6e-a2df-3fdc0b9d8cb7" />

<p>

**Click Install↓**
 
</p>


<img width="578" height="447" alt="Azure step 73" src="https://github.com/user-attachments/assets/79bbbd9e-9192-4f9d-aa70-2b2576417aa4" />

<p>

**Installation Complete, Click Close↓**
 
</p>



<img width="587" height="453" alt="Azure step 74" src="https://github.com/user-attachments/assets/3da184ee-c107-4f29-b144-8ecd4d8b9ec3" />

<p>

**Click the Flag with the caution sign on the right side of Server Manager and Click Promote this server to a domain controller ↓**
 
</p>



<p>
<img width="359" height="326" alt="Azure step 75" src="https://github.com/user-attachments/assets/a8e2a80a-2b3e-43aa-a6da-53dce7753f65" />
</p>

<p>

**Click Add a new forest and Specify the domain information for this operation↓**

<p>
 Root domain name: mydomain.com
</p>
 
</p>



<img width="758" height="557" alt="Azure step 76" src="https://github.com/user-attachments/assets/3bf2149e-4f72-4587-9008-188acd1492f7" />



<img width="759" height="557" alt="Azure step 77" src="https://github.com/user-attachments/assets/e4211474-1c25-4ca6-bce2-ced45e9f3c4d" />



<img width="753" height="528" alt="Azure step 78" src="https://github.com/user-attachments/assets/089efa1f-072a-4543-a335-126a7d3f81c5" />


<img width="754" height="525" alt="Azure step 79" src="https://github.com/user-attachments/assets/b5118327-daad-47c0-8ed5-9d8fcdf1c957" />



<img width="749" height="510" alt="Azure step 80" src="https://github.com/user-attachments/assets/9c10c654-dd2a-440c-928b-98b865136bd2" />



<img width="743" height="514" alt="Azure step 81" src="https://github.com/user-attachments/assets/c2475b52-6129-496d-bcfe-09625ced4a6e" />


<img width="757" height="524" alt="Azure step 82" src="https://github.com/user-attachments/assets/4b41a1da-cf48-4e9b-9ca6-643630ce6a22" />


<p>
<img width="275" height="161" alt="Azure step 83" src="https://github.com/user-attachments/assets/a90914b5-ea95-4262-8448-ed0dea4b94b2" />
</p>
<p>
  <img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/627c75db-dc87-4f7a-b307-6a91ae95888b" />
</p>

<img width="434" height="151" alt="Azure step 84" src="https://github.com/user-attachments/assets/168d4b3e-b8bc-47ab-b703-f8cf379816cb" />
<p>
<img width="309" height="674" alt="Azure step 85" src="https://github.com/user-attachments/assets/03f177a3-0c4e-4fe9-a78e-183328dcd724" />
</p>
<p>
  <img width="260" height="210" alt="Azure step 86" src="https://github.com/user-attachments/assets/b0a4cc58-8c0e-43e8-bf85-5e0ff21bc41a" />
</p>
<img width="633" height="514" alt="Azure step 87" src="https://github.com/user-attachments/assets/4a9d96f2-897a-4ae4-957d-b367262c62dd" />
<img width="430" height="372" alt="Azure step 88" src="https://github.com/user-attachments/assets/f10a60d1-b144-46df-a9e0-0fbfd65e76ba" />
<img width="619" height="507" alt="Azure step 89" src="https://github.com/user-attachments/assets/2ca6dd23-5579-4c57-9f5e-dea7590f4ead" />
<img width="436" height="371" alt="Azure step 90" src="https://github.com/user-attachments/assets/92f90c2c-f377-4dee-b1a6-5785e08bbd00" />

<p>
<img width="97" height="19" alt="Azure step 91" src="https://github.com/user-attachments/assets/032e4efd-9d8a-4fef-9278-fdf04dc9a384" />
</p>

<p>
<img width="449" height="319" alt="Azure step 92" src="https://github.com/user-attachments/assets/6b14173f-9455-469f-92df-6e635acd6d26" />
</p>

<p>
<img width="428" height="372" alt="Azure step 93" src="https://github.com/user-attachments/assets/b3670aa3-47b1-45cb-bd0c-6438d3cc888d" />
</p>


<p> 
<img width="431" height="372" alt="Azure step 94" src="https://github.com/user-attachments/assets/0c826a0a-5024-4617-8a49-e05cdbcce317" />
</p>

<p>
<img width="428" height="370" alt="Azure step 95" src="https://github.com/user-attachments/assets/530282e4-36fe-4eb6-a6bf-43c463428468" />
</p>


<p>
<img width="411" height="356" alt="Azure step 96" src="https://github.com/user-attachments/assets/8f0d4454-aaf6-4793-962e-b16b6790f3f6" />
</p>

<p> 
<img width="391" height="275" alt="Azure step 97" src="https://github.com/user-attachments/assets/4adbbdb2-a81f-445d-b052-38df3fac383e" />
</p> 

<p>
<img width="449" height="242" alt="Azure step 98" src="https://github.com/user-attachments/assets/085cf907-1ea6-4686-b35a-402fb902fcfc" />
</p>

<img width="402" height="473" alt="Azure step 99" src="https://github.com/user-attachments/assets/6564cc2a-d360-408e-8e94-bd95c2d2772c" />
<p>
<img width="380" height="209" alt="Azure step 100" src="https://github.com/user-attachments/assets/efa3a978-2b5d-46ed-a1b8-3449fbdb1c9e" />
</p>

<p>
<img width="220" height="153" alt="Azure step 101" src="https://github.com/user-attachments/assets/c63af1e1-252c-4353-ba9a-774932df950c" />
</p>

<img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/d3e38648-282b-4195-b57a-73bb209c7537" />
<p>
<img width="430" height="151" alt="Azure step 100" src="https://github.com/user-attachments/assets/f3890ba0-5e0e-4bee-9377-4361957ecaff" />
</p>
<p>
<img width="367" height="213" alt="Azure step 102" src="https://github.com/user-attachments/assets/66245173-b83a-44b5-b531-2044e0ca4174" />
</p>
<p>
<img width="430" height="154" alt="Azure step 103" src="https://github.com/user-attachments/assets/1f06c7c1-f371-4982-ab6f-8b718e959bfb" />
</p>

<p>
<img width="226" height="617" alt="Azure step 107" src="https://github.com/user-attachments/assets/1a765018-2941-4b94-9ed6-8131cf2ffd56" />
</p>
<p>
<img width="1039" height="427" alt="Azure step 108" src="https://github.com/user-attachments/assets/29932008-dd9b-44ab-85ab-22fd378dfc23" />
</p>

<p>
<img width="405" height="459" alt="Azure step 109" src="https://github.com/user-attachments/assets/e61d3ba5-26db-4cf8-b54c-56ea994856d0" />
</p>

<p>
<img width="317" height="392" alt="Azure step 110" src="https://github.com/user-attachments/assets/2b3de9d0-63cc-4d0c-a7e8-fe34ef569736" />
</p>
<p>
<img width="445" height="364" alt="Azure step 111" src="https://github.com/user-attachments/assets/588bcc9a-f6d2-45f5-8264-70a3d6767bd9" />
</p>
<p>
<img width="296" height="143" alt="Azure step 112" src="https://github.com/user-attachments/assets/e5366a1a-ed9a-4c42-ab26-8ad6554cf3f7" />
</p>
<p>
<img width="344" height="172" alt="Azure step 113" src="https://github.com/user-attachments/assets/aba1fffd-e620-4248-a265-c1fbaaec6563" />
</p>
<p>
<img width="351" height="169" alt="Azure step 114" src="https://github.com/user-attachments/assets/cfcf42f3-ae88-4991-811d-4fe24b6cdb34" />
</p>
<p>
<img width="357" height="291" alt="Azure Azure" src="https://github.com/user-attachments/assets/bc790620-5e67-4930-b91c-0e7f4f29022c" />
</p>
<p>
<img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/46e5665d-6009-49d3-9d25-52e5898e3d8a" />
</p>
<p>
<img width="430" height="151" alt="Azure step 106" src="https://github.com/user-attachments/assets/a39563af-d511-41a3-8228-1d821ee6c4f7" />
</p>
<p>
<img width="331" height="679" alt="Azure step 115" src="https://github.com/user-attachments/assets/ff1ba640-e2c8-45b5-9ff6-6201f985c7ae" />
</p>
<p>
<img width="276" height="93" alt="Azure step 116" src="https://github.com/user-attachments/assets/1050d8a4-5b3d-42ef-a2b3-f2d77ef12200" />
</p>
<p>
<img width="159" height="21" alt="Azure step 117" src="https://github.com/user-attachments/assets/81532077-ac3e-4fcb-8aa9-09f1d43c09ab" />
</p>
<p>
<img width="635" height="342" alt="Azure step 118" src="https://github.com/user-attachments/assets/63f5412d-a6d2-40f4-8c21-fd0d32e2f66f" />
</p>
<p>
<img width="97" height="17" alt="Azure step 119" src="https://github.com/user-attachments/assets/bad9ff58-7bef-49fd-b473-f2af0e092c9b" />
</p>
<p>
<img width="867" height="400" alt="Azure step 120" src="https://github.com/user-attachments/assets/deef0c17-fddf-4440-9aad-e9e655d36ade" />
</p>
<p>
<img width="370" height="231" alt="Azure step 121" src="https://github.com/user-attachments/assets/e84af216-3c93-4a5c-9d1c-97019f29bee2" />
</p>
<p>
<img width="432" height="152" alt="Azure step 122" src="https://github.com/user-attachments/assets/6ab8918e-a114-48a3-93be-aa23ff6becc5" />
</p>
<p>
<img width="212" height="619" alt="Azure step 123" src="https://github.com/user-attachments/assets/13dc1eaf-324e-4b0f-8188-12ad506e3b28" />
</p>
<p>
<img width="333" height="55" alt="Azure step 124" src="https://github.com/user-attachments/assets/d7c4428d-4c8e-4499-8424-035be6ca3451" />
</p>
<p>
<img width="344" height="62" alt="Azure step 125" src="https://github.com/user-attachments/assets/02ed81ca-39a2-4310-84c6-f421c647a2fd" />
</p>
<p>
<img width="370" height="323" alt="Azure step 126" src="https://github.com/user-attachments/assets/b5d68dc0-16eb-4b3f-9b1c-fa4991d557c5" />
</p>
<p>
<img width="452" height="242" alt="Azure step 127" src="https://github.com/user-attachments/assets/29b488bd-9351-42ee-84b8-72999c76aa3b" />
</p>
<p>
<img width="373" height="327" alt="Azure step 128" src="https://github.com/user-attachments/assets/fef980c9-e556-451b-8f72-722f1188c266" />
</p>
<p>
<img width="391" height="258" alt="Azure" src="https://github.com/user-attachments/assets/ab339eeb-efbe-44db-b167-0ac88dcd1062" />
</p>
<p>
<img width="432" height="152" alt="Azure step 122" src="https://github.com/user-attachments/assets/56b1f18f-d948-4f10-95e9-5848f6611e74" />
</p>
<p>
<img width="425" height="663" alt="Azure step 129" src="https://github.com/user-attachments/assets/09325f03-bfe8-4330-a59f-cccb7617e48a" />
</p>
<p>
<img width="714" height="87" alt="Azure step 130" src="https://github.com/user-attachments/assets/b82d8c0a-6872-4cca-979b-3be215695eb9" />
</p>
<p>
<img width="1064" height="732" alt="Azure step 131" src="https://github.com/user-attachments/assets/b9a8665e-58ef-4f3a-a658-875fecdc09ed" />
</p>
<p>
<img width="947" height="370" alt="Azure step 132" src="https://github.com/user-attachments/assets/71c03ffa-0af4-4d80-9ef9-27dbca9e2316" />
</p>
<p>
<img width="704" height="465" alt="Azure step 133" src="https://github.com/user-attachments/assets/853105f7-9f2e-419e-b58c-9b9627555bf2" />
</p>
<p>
<img width="252" height="171" alt="Azure step 134" src="https://github.com/user-attachments/assets/c78eb757-11bb-4204-b29b-7a3264f5ebae" />
</p>
<p>
<img width="1403" height="348" alt="Azure step 135" src="https://github.com/user-attachments/assets/300bb5a4-e861-4207-bb21-4f88034caf52" />
</p>
<p>
<img width="134" height="75" alt="Azure step 136" src="https://github.com/user-attachments/assets/6e104aa5-e45e-4adc-8948-0629eb19d5e9" />
</p>
<p>
<img width="445" height="105" alt="Azure step 137" src="https://github.com/user-attachments/assets/410d1318-68a8-479e-aaaf-25601b34d6a3" />
</p>
<p>
<img width="500" height="325" alt="Azure step 138" src="https://github.com/user-attachments/assets/88c9c74b-5627-4e8e-aaf7-484b99ebb69c" />
</p>
<p>
<img width="712" height="615" alt="Azure step 139" src="https://github.com/user-attachments/assets/498881b5-50f5-47d8-abc3-7f629ea2b1af" />
</p>
<p>
<img width="432" height="148" alt="Azure step 144" src="https://github.com/user-attachments/assets/773ac60d-f92d-42cb-ac1c-979816ff403d" />
</p>
<p>
<img width="345" height="466" alt="Azure step 145" src="https://github.com/user-attachments/assets/333e08d6-06e5-4ef4-9dd6-0ac6ce181cbc" />
</p>
<p>
<img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/6f8af8d9-febf-4251-adfb-f88c1631f569" />
</p>
<p>
<img width="309" height="674" alt="Azure step 85" src="https://github.com/user-attachments/assets/a5259283-143b-499c-9844-4f5a0517c6f5" />
</p>
<p>
<img width="260" height="210" alt="Azure step 86" src="https://github.com/user-attachments/assets/970b7a43-f704-4a2e-8884-74f1624cee33" />
</p>
<p>
<img width="341" height="64" alt="Azure step 143" src="https://github.com/user-attachments/assets/d762d3b1-e1df-4328-af63-3f26e51d15f0" />
</p>
<p>
<img width="379" height="222" alt="Azure step 30" src="https://github.com/user-attachments/assets/1d17ef95-50b9-4b8c-9cfb-cb376e51c2ea" />
</p>
<p>
<img width="432" height="148" alt="Azure step 144" src="https://github.com/user-attachments/assets/f92bfe13-2077-42ee-b625-f600bee6e70b" />
</p>
configure group policy
<p>
<img width="245" height="534" alt="Screenshot 2026-03-03 at 2 16 13 AM" src="https://github.com/user-attachments/assets/e89f6f23-0753-4aaa-a80d-23cafa7e9a09" />
</p>
<p>
<img width="366" height="188" alt="Screenshot 2026-03-03 at 2 17 16 AM" src="https://github.com/user-attachments/assets/022f1ef5-2492-4564-9a8f-4c4036ab13f1" />
</p>
<p>
<img width="434" height="711" alt="Screenshot 2026-03-03 at 2 19 28 AM" src="https://github.com/user-attachments/assets/4c0186c0-0107-4279-859d-f4345c25db84" />
</p>
<p>
<img width="726" height="478" alt="Screenshot 2026-03-03 at 2 21 54 AM" src="https://github.com/user-attachments/assets/4aca44f9-b768-422b-85b2-5a029b778e2e" />
</p>
<p>
<img width="548" height="442" alt="Screenshot 2026-03-03 at 2 35 52 AM" src="https://github.com/user-attachments/assets/ff61d9ae-6cf5-47f3-b245-691830da7c88" />
</p>
<p>
<img width="382" height="468" alt="Screenshot 2026-03-03 at 2 38 07 AM" src="https://github.com/user-attachments/assets/1e0b54f9-5f2b-4a50-90de-5ac56d495173" />
</p>
<p>
<img width="472" height="240" alt="Screenshot 2026-03-03 at 2 49 16 AM" src="https://github.com/user-attachments/assets/7370c2d0-7f2f-48a8-8343-fb7be5eb4a8e" />
</p>
<p>
<img width="512" height="136" alt="Screenshot 2026-03-03 at 2 51 04 AM" src="https://github.com/user-attachments/assets/e6ced7d5-ef8c-4bbb-baf3-ea2326c6553f" />
</p>
<p>
<img width="364" height="220" alt="Screenshot 2026-03-03 at 2 57 59 PM" src="https://github.com/user-attachments/assets/2ba0b71b-c141-4158-92b2-b82f9fac4e17" />
</p>
<p>
<img width="507" height="170" alt="Screenshot 2026-03-03 at 4 09 44 PM" src="https://github.com/user-attachments/assets/6c043ac8-3050-4fc3-8eeb-9ae6d6b6d44a" />
</p>
<p>
<img width="430" height="151" alt="Azure step 106" src="https://github.com/user-attachments/assets/cfb261a7-e86b-42dd-ae5e-2f1633376572" />
</p>
<p>
<img width="278" height="401" alt="Screenshot 2026-03-03 at 5 25 30 PM" src="https://github.com/user-attachments/assets/a4c1498d-84cc-4d10-9c81-3aab08ca0a84" />
</p>
<p>
<img width="362" height="622" alt="Screenshot 2026-03-03 at 6 26 35 PM" src="https://github.com/user-attachments/assets/e96d145f-fb8c-41ac-a668-7ea44e4d41cb" />
</p>
<p>
<img width="904" height="475" alt="Screenshot 2026-03-03 at 6 38 02 PM" src="https://github.com/user-attachments/assets/b31de5e5-cb7c-4f8a-9a4b-fec0aeb3e755" />
</p>
<p>
<img width="237" height="324" alt="Screenshot 2026-03-03 at 6 46 06 PM" src="https://github.com/user-attachments/assets/84c1ce79-6b43-4293-bb63-f86eb9e2e766" />
</p>
<p>
<img width="373" height="221" alt="Screenshot 2025-11-20 at 9 27 55 PM" src="https://github.com/user-attachments/assets/6eb79334-8750-4de7-90de-60d62cde6dc8" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
<p>
<img width="426" height="140" alt="Screenshot 2025-11-20 at 9 25 34 PM" src="https://github.com/user-attachments/assets/a9f9f1b3-c0ca-47bb-acd0-ab4d19d80cf3" />
</p>
after 6 failed log in attempts
<p>
<img width="253" height="305" alt="Azure step 142" src="https://github.com/user-attachments/assets/bf531b9f-b6f4-4fd7-98ab-a8cf8516d5eb" />
</p>
<p>
<img width="365" height="59" alt="Azure step 146" src="https://github.com/user-attachments/assets/d3282123-cd81-4ce9-a842-04e73948724f" />
</p>
<p>
<img width="509" height="473" alt="Azure step 147" src="https://github.com/user-attachments/assets/a55794fb-bf7a-4188-b2e7-820d20011ed1" />
</p>
<p>
<img width="405" height="531" alt="Azure step 148" src="https://github.com/user-attachments/assets/be122f64-6dc8-47ef-a613-95d32ed677c7" />
</p>









<p>
<img width="507" height="305" alt="Screenshot 2025-11-20 at 9 11 19 PM" src="https://github.com/user-attachments/assets/fd0a6b5c-6126-48f8-9080-c6fd6f03842c" />
</p>
<p>
<img width="513" height="140" alt="Screenshot 2025-11-20 at 9 11 47 PM" src="https://github.com/user-attachments/assets/49106e91-89c4-4189-9be4-4e3647b8b5cf" />
</p>
<p>
<img width="376" height="249" alt="Screenshot 2025-11-20 at 9 13 23 PM" src="https://github.com/user-attachments/assets/97da55d1-1d9e-4697-b9d2-5cbcb1f2a2f3" />
</p>
<p>
<img width="511" height="427" alt="Screenshot 2025-11-20 at 9 21 25 PM" src="https://github.com/user-attachments/assets/2e359962-7766-4afb-aba0-0eda20e86803" />
</p>
<p>
<img width="365" height="220" alt="Screenshot 2026-03-05 at 10 24 11 PM" src="https://github.com/user-attachments/assets/d06fc819-3d67-4ffc-8751-929b783155f2" />
</p>
<p>
<img width="432" height="148" alt="Azure step 144" src="https://github.com/user-attachments/assets/99b120b4-7eee-4812-98d2-3ba0b6a726d7" />
</p>
<p>
<img width="247" height="263" alt="Screenshot 2025-11-20 at 9 25 48 PM" src="https://github.com/user-attachments/assets/603e4641-b178-45e8-b274-10565bca59f4" />
</p>
<p>
<img width="516" height="436" alt="Screenshot 2025-11-20 at 9 27 19 PM" src="https://github.com/user-attachments/assets/372e98de-b4a6-41eb-90c3-eafa8f84ef80" />
</p>
<p>
<img width="432" height="148" alt="Azure step 144" src="https://github.com/user-attachments/assets/7d29ca1f-d175-4978-8ba5-1ebc94a707a0" />
</p>
<p>
<img width="345" height="466" alt="Azure step 145" src="https://github.com/user-attachments/assets/93e11b48-93fb-4eef-bbce-519c175dce1f" />
</p>


<p>
<img width="364" height="232" alt="Screenshot 2026-03-06 at 2 18 11 AM" src="https://github.com/user-attachments/assets/fe923759-8541-4977-b090-8cecb0841b9d" />
</p>
<P>
<img width="318" height="675" alt="Screenshot 2025-11-20 at 9 34 21 PM" src="https://github.com/user-attachments/assets/af1fdfd0-05ba-4ec0-aae7-cb700ae726a9" />
</P>
<P>
<img width="199" height="226" alt="Screenshot 2025-11-20 at 9 34 50 PM" src="https://github.com/user-attachments/assets/85a2294c-7f69-4ef8-8994-c52ab3f4c036" />
</P>
<p>
<img width="298" height="174" alt="Screenshot 2025-11-20 at 9 35 35 PM" src="https://github.com/user-attachments/assets/8ef9a564-529d-4b80-8d2b-2bf3f93592ab" />
</p>
<p>
<img width="420" height="121" alt="Screenshot 2025-11-20 at 9 35 49 PM" src="https://github.com/user-attachments/assets/6b1255c8-55cb-4b1e-83fc-9fa9b8d13cb5" />
</p>
<p>
<img width="365" height="220" alt="Screenshot 2026-03-05 at 10 24 11 PM" src="https://github.com/user-attachments/assets/9e9797ca-bc0a-4fd2-9654-1975f4486390" />
</p>
<p>
<img width="651" height="215" alt="Screenshot 2025-11-20 at 10 47 14 PM" src="https://github.com/user-attachments/assets/55e42695-8912-4658-b92b-c17edba7a04b" />
</p>
<p>
<img width="449" height="584" alt="Screenshot 2025-11-20 at 10 49 35 PM" src="https://github.com/user-attachments/assets/ce449dda-316b-4c5b-b6e4-8365063ffddf" />
</p>
<p>
<img width="818" height="164" alt="Screenshot 2025-11-20 at 11 07 28 PM" src="https://github.com/user-attachments/assets/069b0a46-3a26-4862-8656-82d04bf4431b" />
</p>
<p>
<img width="892" height="175" alt="Screenshot 2025-11-20 at 11 10 45 PM" src="https://github.com/user-attachments/assets/50184b7e-a461-419e-803f-4481b71b518e" />
</p>
