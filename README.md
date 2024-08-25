# Human Resource Dashboard

Dashboard ini merupakan salah satu rangkaian dalam proses magang virtual saya di PwC Switzerland - Power BI Job Simluation

## Table of Contents:

- Business Background
- Dataset
- Objective
- Measure
- Dashboard
- Insight
  
## Business Background
Sumber Daya Manusia di klien telekomunikasi kami sangat memperhatikan keberagaman dan inklusi. Mereka telah bekerja keras untuk meningkatkan keseimbangan gender di tingkat manajemen eksekutif, tetapi mereka tidak melihat adanya kemajuan. Mereka meminta bantuan kami. Di PwC Swiss, kami sering didekati oleh klien yang mencari dukungan dalam hal keragaman dan inklusi. Perusahaan membutuhkan tenaga kerja dengan beragam talenta dan latar belakang untuk dapat sukses di dunia yang semakin kompleks dan heterogen. Bagi kami, keragaman dan inklusi adalah keharusan bisnis, bukan hanya sekedar keinginan. Kami ingin agar semua tim kami merasa diterima dan dihargai. Namun, untuk mencapai hal ini dan membuka potensinya, ada banyak tantangan praktis yang harus dihadapi.

## Dataset
Dataset yang digunakan untuk tugas ini disajikan oleh Pwc dan sumber dataset diversity & inclusion: [dataset](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fcdn.theforage.com%2Fvinternships%2Fcompanyassets%2F4sLyCPgmsy8DA6Dh3%2F03%2520Diversity-Inclusion-Dataset.xlsx&wdOrigin=BROWSELINK)

## Objective
- Bagaimana menentukan indikator kinerja utama (KPI) yang terkait dengan keseimbangan dan keragaman gender.
- Cara membuat visualisasi yang merepresentasikan data SDM secara efektif.
- Pentingnya keragaman dan inklusi dalam dunia perusahaan.

## Measure
- Jumlah Pria = `Calculate(distinctcount('Pharma Group AG'[Employee ID]),Filter('Pharma Group AG','Pharma Group AG'[Gender]="Male"))`
- Jumlah Wanita = `Calculate(distinctcount('Pharma Group AG'[Employee ID]),Filter('Pharma Group AG','Pharma Group AG'[Gender]="Female"))`
- Persentase rekrut Pria = `Divide('Pharma Group AG'[Jumlah Pria],('Pharma Group AG'[Jumlah Pria]+'Pharma Group AG'[Jumlah Wanita]))`
- Persentase rekrut Wanita = `Divide('Pharma Group AG'[Jumlah Wanita],('Pharma Group AG'[Jumlah Wanita]+'Pharma Group AG'[Jumlah Pria]))`
- Performance Pria = `Calculate(Average('Pharma Group AG'[FY20 Performance Rating]),Filter('Pharma Group AG','Pharma Group AG'[Gender]="Male"))`
- Performance Wanita = `Calculate(Average('Pharma Group AG'[FY20 Performance Rating]),Filter('Pharma Group AG','Pharma Group AG'[Gender]="Female"))`
- Turnover rate = `Divide(Calculate(distinctcount('Pharma Group AG'[Employee ID]),Filter('Pharma Group AG','Pharma Group AG'[FY20 leaver?]="Yes")),Divide(Calculate(distinctcount('Pharma Group AG'[Employee ID]),Filter('Pharma Group AG','Pharma Group AG'[In base group for turnover FY20]="Y"))+Calculate(distinctcount('Pharma Group AG'[Employee ID]),Filter('Pharma Group AG',NOT('Pharma Group AG'[Department @01.07.2020]=BLANK()))),2))`

## Dashboard
![image](https://github.com/user-attachments/assets/684f20f8-9296-4c3c-9fcf-e0b53f7028a2)

## Insight
- 41 % wanita direkrut dan 59 % pria yang direkrut pada FY20.
- Department Finance memiliki turnover paling tinggi sebesar 22%.
- Average Rating Female 2.42% and Average Rating Male 2.41%
- Terdapat 47 karyawan yang meninggalkan perusahaan (26 pria dan 21 wanita)
- Kelompok usia yang paling banyak adalah 20-29 tahun dengan 223 karyawan yang termasuk dalam kategori ini.



