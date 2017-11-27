---
title: "Držitelé zálohy"
description: "Poznejte funkce držitelů záloh v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: LizaGolub
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262574
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 36b6d74d29ed4606c1b501b68e0f2253e66c8eb6
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="advance-holders"></a>Držitelé zálohy

[!include[banner](../includes/banner.md)]


Poznejte funkce držitelů záloh v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

*Držitel zálohy* je zaměstnanec společnosti, který je zodpovědný za částku výdajů, kterou poskytuje organizace. Pouze pracovník společnosti může být držitelem zálohy. Pokud dojde k pořízení, držitel zálohy nahlásí společnosti uskutečněné výdaje. Společnost refunduje zaměstnanci částku výdajů. Společnost kontroluje zůstatek pro každého držitele zálohy. Uživatelé v právnických osobách v Estonsku, Lotyšsku, Litvě, Polsku, České republice, Maďarsku a Rusku mohou reflektovat určité transakce doprovázející operace se zaměstnanci společnosti, kteří jsou odpovědní za částku výdajů poskytovanou organizací.

## <a name="set-up-an-advance-holder"></a>Nastavení držitele záloh
Pokud chcete nastavit držitele zálohy, je třeba provést následující úkoly v daném pořadí.
1.  Vytvořte skupiny držitelů záloh.
2.  Nastavte účetní profil zaměstnance.
3.  Nastavte parametry závazků.
4.  Vytvořte specifické podmínky platby pro držitele zálohy.
5.  Vytvořte držitele záloh.

### <a name="advance-holder-groups"></a>Skupiny držitelů záloh

Použijte stránku **Skupiny držitelů záloh** k vytvoření skupiny držitelů záloh. Můžete zadat název, popis a protiúčet pro skupinu držitelů záloh.
### <a name="employee-posting-profile"></a>Účetní profil zaměstnance

Použijte stránku **Účetní profily zaměstnanců** k vytvoření profilu pro transakce držitelů záloh. Můžete zadat následující informace pro účetní profil zaměstnance.
|Pole |popis|
|------|-----------|
|Účetní profil|Zadejte identifikační kód účetního profilu držitele zálohy.|
|popis|Zadejte stručný popis účetního profilu.|
|Platné pro|Vyberte jednu z následujících možností pro úroveň seskupení pro nastavení účetního profilu: 
**Tabulka** – tuto možnost lze použít k nastavení účetního profilu pro jednoho držitele zálohy. Je třeba určit kód držitele zálohy v poli Odkaz.
**Skupina** – tuto možnost lze použít k nastavení účetního profilu pro skupinu držitelů záloh. Je třeba určit kód skupiny v poli Odkaz.
**Všechny** – tato možnost slouží k nastavení účetního profilu pro všechny držitele záloh. | |Odkaz| Vyberte kód držitele zálohy, pokud je vybrána Tabulka v poli Platné pro, nebo vyberte skupinu držitelů záloh, pokud je vybrána Skupina v poli Platné pro. | |Součtový účet| Vyberte součtový účet pro zaúčtování transakce.|



### <a name="account-payable-parameters"></a>Parametry závazku

Pokud chcete, aby se projevily transakce držitele zálohy, musíte nastavit následující položky na stránce **Parametry závazků** v části **Držitelé zálohy**.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Pole**                                     | **Popis**                                                                                                                                                                  |
| **Účetní profil**                            | Vyberte výchozí profil pro dokončení transakce držitelů záloh.                                                                                                         |
| **Řazení držitelů záloh**                     | Je-li tato možnost vybrána, držitelé zálohy se zobrazí na začátku seznamu na stránce **Držitelé zálohy**.                                                                     |
| **Výdej v případě otevřeného zůstatku**                 | Je-li tato možnost vybrána, bude povoleno vydání hotovostní zálohy držiteli zálohy, který má otevřený kladný zůstatek.                                                                      |
| **Uzavření zůstatku pomocí skupiny polí hotovosti: název** | Vyberte kód deníku pokladního dokladu. Tento kód deníku slouží ke generování hotovostních výdajových dokladů a refundačních dokladů při uzavření zůstatků držitele zálohy prostřednictvím hotovosti. |
| **Hotovost**                                       | Zvolte pokladní účet, chcete-li určit doklady, které se používají pro uzavření zůstatků držitele zálohy.                                                                 |
| **Uzavření zůstatku pomocí skupiny polí banky: název** | Vyberte kód deníku pro transakce k uzavření zůstatku prostřednictvím banky.                                                                                                   |
| **Typ účtu**                               | Vyberte banku pro uzavření zůstatku držitele zálohy prostřednictvím banky.                                                                                                        |
| **Hlavní účet**                               | Vyberte kód bankovního účtu pro uzavření zůstatku držitele zálohy prostřednictvím banky.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Platební podmínky držitele zálohy

Pro správné zaregistrování a zaúčtování nákupní objednávky prostřednictvím držitele zálohy je nutné použít podmínky platby, které byly nastaveny pomocí možnosti **Od držitele zálohy** nastavené na **True**.
### <a name="create-an-advance-holder-creation"></a>Vytvoření držitelů záloh

Před vytvořením držitele zálohy musí mít již nastavené pracovníky. Další informace naleznete v tématu [Zadání informací o pracovníkovi (průvodce záznamem úloh).](../../fin-and-ops/hr/tasks/enter-worker-information.md) Použijte stránku **Držitelé zálohy** k nastavení pracovníka jako držitele zálohy. Vyberte pracovníka, kterého chcete použít jako držitele zálohy, klikněte na možnost **Upravit** a potom nastavte možnost **Držitel zálohy** na **True**. Dále je nutné vyplnit následující pole.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Pole**      | **Popis**                                                                             |
| **Skupina**      | Vyberte skupinu držitelů záloh.                                                             |
| **Řada**     | Zadejte řadu dokladu, která slouží k ověření totožnosti držitele zálohy. |
| **Číslo**     | Zadejte číslo dokladu, které slouží k ověření totožnosti držitele zálohy. |
| **Datum vydání** | Vyberte nebo zadejte datum vydání dokumentu.                                                    |
| **Vydal**  | Zadejte podrobnosti o orgánu nebo osobě, která dokument vydala.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Dotazy a sestavy držitele zálohy
### <a name="advance-holder-transactions-inquiry"></a>Dotaz na transakce držitelů záloh

Seznam transakcí držitele zálohy získáte kliknutím na tlačítko **Transakce** na stránce **Držitelé zálohy**. Chcete-li zobrazit transakce pro všechny držitele záloh nebo vytvořit konkrétní dotaz založený na transakcích držitelů záloh, klikněte na **Závazky**&gt;**Dotazy a sestavy**&gt;**Dotazy a sestavy držitelů záloh**&gt; Transakce. Kliknutím na možnost **Řádky** otevřete stránku **Transakce dokladu**.
### <a name="advance-holder-balance-inquiry"></a>Dotaz na zůstatek držitele zálohy

Použijte stránku **Držitelé zálohy** k zobrazení zůstatku držitele zálohy. Chcete-li zobrazit zůstatek pro všechny držitele záloh nebo vytvořit konkrétní dotaz založený na účtech držitelů záloh, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Zůstatek.**
### <a name="advance-holder-balance-report"></a>Sestava zůstatku držitele zálohy

Chcete-li zobrazit a vytisknout sestavu na základě informací o zůstatku držitele zálohy, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Sestava zůstatku držitele zálohy.**
### <a name="advance-holder-transactions-report"></a>Sestava transakcí držitelů záloh

Chcete-li zobrazit a vytisknout sestavu na základě transakcí držitele zálohy, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Sestava transakcí držitelů záloh.**

## <a name="advance-holder-transactions"></a>Transakce držitelů záloh

Poznejte, jak pracovat s transakcemi držitelů záloh v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Transakce pro tyto pracovníky, kteří jsou držitelé zálohy, mohou být zaúčtovány pomocí účtů držitele zálohy. ID pracovníka, které je určeno pro každého držitele zálohy, lze použít ke sledování všech transakcí držitele zálohy. Toto číslo je načteno jako číslo účtu pro transakce držitele zálohy na stránkách **Hlavní deníky** a **Transakce držitele zálohy**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Tvorba a zaúčtování nákupních objednávek s podrobnostmi o držiteli zálohy
Další obecné informace o nákupních objednávkách naleznete v tématu [Přehled nákupních objednávek](../../supply-chain/procurement/purchase-order-overview.md). Pokud je faktura dodavatele vytvořena a zaúčtována s podrobnostmi držitele zálohy, zůstatky držitele zálohy budou zaúčtovány do účtu zůstatku zaměstnance namísto do účtu zůstatku dodavatele. Chcete-li přidat podrobnosti držitele zálohy k nákupní objednávce, postupujte takto:

-   V poli **Platební podmínky** v části **Ceny a slevy** vyberte platební podmínku. <!---For more information about **Terms of payment**, see [Define vendor payment terms](accounts-payable/tasks/define-vendor-payment-terms).-->Vyberte platební podmínku, která má na stránce **Platební podmínky** vybranou možnost **Od držitele zálohy**. Další informace o nastavení platebních podmínek pro držitele záloh naleznete v tématu [Držitelé zálohy](emea-advance-holders.md).
-   V poli **Držitel zálohy** na pevné záložce **Ceny a slevy** vyberte držitele zálohy pro nákupní objednávku.

Proces zaúčtování nákupní objednávky vytvoří dvě transakce dodavatele s opačným částkami a jednu transakci držitele zálohy. Bez podrobností držitele zálohy je vytvořena pouze jedna transakce dodavatele.

### <a name="settle-advance-holder-balances-via-a-bank"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím banky
Když vyrovnáte zůstatky držitelů záloh prostřednictvím banky, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v hlavním deníku. Můžete nastavit kód pro deník a banky v části **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Držitelé záloh](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím banky, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v bance**. Na stránce **Uzavřít v bance** zadejte následující informace.

| Pole                    | popis |
|------------------------------|-------------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.|

### <a name="settle-advance-holder-balances-via-cash"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím hotovosti
Když vyrovnáte zůstatky držitelů záloh prostřednictvím hotovosti, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v deníku dokladů. Můžete nastavit kód pro deník a hotovost na kartě **Držitelé záloh** na stránce **Parametry závazků**. Další informace naleznete v tématu [Držitelé záloh](emea-advance-holders.md). Pro uzavření zůstatku držitele zálohy prostřednictvím hotovosti, otevřete **Závazky**&gt;**Držitelé záloh**&gt;**Držitelé záloh**. Klikněte na tlačítko **Zůstatek** v podokně akcí a pak klikněte na tlačítko **Uzavřít v hotovosti**. Na stránce **Uzavřít v hotovosti** zadejte následující informace.

| Pole                    | popis
|------------------------------|-----------------|
| **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
| **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** ve formuláři **Zůstatek**, je ve výchozím nastavení zobrazena. |
| **Automaticky**                | Vyberte zaškrtávací políčko **Automaticky** pro automatické vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.     |

Po zpracování deníku dokladů, pokud částka v poli **Převáděná částka** je záporná, výdajový doklad je vygenerován pro držitele zálohy při uzavření zůstatků. Pokud částka v poli **Převáděná částka** byla pozitivní, vygeneruje se refundační doklad.

## <a name="additional-resources"></a>Další zdroje

- [Záloha pro zaměstnance (východní Evropa)](tasks/advance-payment-employee.md)




