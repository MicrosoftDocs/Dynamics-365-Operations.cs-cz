---
title: Přehled držitelů záloh
description: Toto téma obsahuje informace o funkci držitele zálohy.
author: liza-golub
ms.date: 09/15/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.reviewer: kfend
ms.custom:
- "262574"
- intro-internal
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ed09542e3f369a079c60c17a02f4d08c9f8a9e99
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984947"
---
# <a name="advance-holders-overview"></a>Přehled držitelů záloh

[!include [banner](../includes/banner.md)]

*Držitel zálohy* je zaměstnanec společnosti, který je zodpovědný za částku výdajů, kterou poskytuje organizace. Pouze pracovník společnosti může být držitelem zálohy. Pokud dojde k pořízení, držitel zálohy nahlásí společnosti uskutečněné výdaje. Společnost refunduje zaměstnanci částku výdajů. Společnost kontroluje zůstatek pro každého držitele zálohy. Uživatelé v právnických osobách v Estonsku, Lotyšsku, Litvě, Polsku, České republice, Maďarsku a Rusku mohou reflektovat určité transakce doprovázející operace se zaměstnanci společnosti, kteří jsou odpovědní za částku výdajů poskytovanou organizací.

## <a name="set-up-an-advance-holder"></a>Nastavení držitele záloh
Dokončete následující úkoly, abyste nastavili držitele zálohy. Ujistěte se, že tyto úkoly dokončíte v uvedeném pořadí.

1. Vytvořte skupiny držitelů záloh.
2. Nastavte účetní profil zaměstnance.
3. Nastavte parametry závazků.
4. Vytvořte specifické platební podmínky pro držitele záloh.
5. Vytvořte specifické platební podmínky pro držitele záloh.
6. Vytvořte držitele zálohy.


### <a name="advance-holder-groups"></a>Skupiny držitelů záloh

Použijte stránku **Skupiny držitelů záloh** k vytvoření skupiny držitelů záloh. Můžete zadat název, popis a protiúčet pro skupinu držitelů záloh.
### <a name="employee-posting-profile"></a>Účetní profil zaměstnance

Použijte stránku **Účetní profily zaměstnanců** k vytvoření profilu pro transakce držitelů záloh. Můžete zadat následující informace pro účetní profil zaměstnance.

|      Pole      |                                            popis                                            |
|-----------------|---------------------------------------------------------------------------------------------------|
| **Účetní profil** |  Zadejte identifikační kód účetního profilu držitele zálohy.               |
|   **popis**   |  Zadejte stručný popis účetního profilu.                         |
|    **Platné pro**    |  Vyberte jednu z následujících možností pro úroveň seskupení pro nastavení účetního profilu: <ul> <li>**Tabulka** – tuto možnost lze použít k nastavení účetního profilu pro jednoho držitele zálohy. Je třeba určit kód držitele zálohy v poli **Reference**.</li> <li>**Skupina** – tuto možnost lze použít k nastavení účetního profilu pro skupinu držitelů záloh. Je třeba určit kód skupiny v poli **Reference**.</li> <li>**Vše** – tuto možnost lze použít k nastavení účetního profilu pro všechny držitele zálohy.</li></ul> |
| **Odkaz** | Vyberte kód zálohy držitele, pokud je vybraná možnost **Tabulka** v poli **Platné pro** nebo vyberte skupinu vlastníků zálohy, pokud je vybraná hodnota **Skupina** v poli **Platné pro**. |
| **Součtový účet** | Vyberte souhrnný účet marže pro zaúčtování transakcí. |



### <a name="account-payable-parameters"></a>Parametry závazku

Pokud chcete, aby se projevily transakce držitele zálohy, musíte nastavit následující pole na stránce **Parametry závazků** v části **Držitelé zálohy**.

|  Pole                                         | Popis       |
|------------------------------------------------|-------------------|
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

### <a name="create-an-advance-holder"></a>Vytvoření držitele zálohy

Před vytvořením držitele zálohy musí mít již nastavené pracovníky. Další informace naleznete v tématu [Zadání informací o pracovníkovi (průvodce záznamem úloh).](../../human-resources/hr-personnel-enter-worker-information.md) 

1. Přejděte na **Závazky** > **Držitelé zálohy** > **Držitelé zálohy**.

    > [!NOTE]
    > Nelze přidat nebo odstranit zaměstnance na stránce **Držitelé záloh**. Zaměstnanci musí být nejprve přijati v modulu **Lidské zdroje**. Na stránce **Účetní profil zaměstnance** můžete nastavit účetní profil zaměstnance, který se používá k účtování zůstatků držitelů záloh.

2. Vyberte zaměstnance a poté zvolte **Upravit**.
3. Na pevné záložce **Obecné** nastavte možnost **Držitel zálohy** na **Ano** pro označení, že zaměstnanec je držitelem zálohy.
4. V poli **Skupina** vyberte skupinu držitele zálohy, ke které zaměstnanec patří.
5. Do možnosti **Osobní doklad** zadejte podrobnosti identifikačního dokumentu.
    - **Řady**: Zadejte řadu dokladu, která slouží k ověření totožnosti držitele zálohy.
    - **Číslo**: Zadejte číslo dokladu, které slouží k ověření totožnosti držitele zálohy.
    - **Datum vydání**: Vyberte nebo zadejte datum vydání dokumentu.
    - **Vydal**: Zadejte podrobnosti o orgánu nebo osobě, která dokument vydala.
6. Zvolte **Uložit** nebo zavřete stránku.

> [!NOTE]
> Pokud je možnost **Řazení držitelů záloh** nastavena na **Ano** na stránce **Parametry závazků**, držitelé záloh se zobrazí v horní části mřížky na stránce **Držitelé záloh**.


## <a name="advance-holder-inquiries-and-reports"></a>Dotazy a sestavy držitele zálohy

### <a name="advance-holder-transactions-inquiry"></a>Dotaz na transakce držitelů záloh

Seznam transakcí držitele zálohy získáte vyberte **Transakce** na stránce **Držitelé zálohy**. Chcete-li zobrazit transakce pro všechny držitele záloh nebo vytvořit konkrétní dotaz založený na transakcích držitelů záloh, přejděte na nabídku **Závazky** > **Dotazy a sestavy** > **Dotazy a sestavy držitelů záloh** > **Transakce**. Výběrem možnosti **Řádky** otevřete stránku **Transakce dokladu**.

### <a name="advance-holder-balance-inquiry"></a>Dotaz na zůstatek držitele zálohy

Použijte stránku **Držitelé zálohy** k zobrazení zůstatku držitele zálohy. Chcete-li zobrazit zůstatek pro všechny držitele záloh nebo vytvořit konkrétní dotaz založený na účtech držitelů záloh, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Zůstatek.**
### <a name="advance-holder-balance-report"></a>Sestava zůstatku držitele zálohy

Chcete-li zobrazit a vytisknout sestavu na základě informací o zůstatku držitele zálohy, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Sestava zůstatku držitele zálohy.**
### <a name="advance-holder-transactions-report"></a>Sestava transakcí držitelů záloh

Chcete-li zobrazit a vytisknout sestavu na základě transakcí držitele zálohy, klikněte na **Závazky** &gt; **Dotazy a sestavy** &gt; **Dotazy a sestavy držitelů záloh** &gt; **Sestava transakcí držitelů záloh.**

## <a name="advance-holder-transactions"></a>Transakce držitelů záloh

Transakce pro pracovníky, kteří jsou držitelé zálohy, mohou být zaúčtovány pomocí účtů držitele zálohy. ID pracovníka, které je určeno pro každého držitele zálohy, lze použít ke sledování všech transakcí držitele zálohy. Toto číslo je načteno jako číslo účtu pro transakce držitele zálohy na stránkách **Hlavní deníky** a **Transakce držitele zálohy**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Tvorba a zaúčtování nákupních objednávek s podrobnostmi o držiteli zálohy
Další obecné informace o nákupních objednávkách naleznete v tématu [Přehled nákupních objednávek](../../supply-chain/procurement/purchase-order-overview.md). Pokud je faktura dodavatele vytvořena a zaúčtována s podrobnostmi držitele zálohy, zůstatky držitele zálohy budou zaúčtovány do účtu zůstatku zaměstnance namísto do účtu zůstatku dodavatele. Chcete-li přidat podrobnosti držitele zálohy k nákupní objednávce, postupujte takto:

1. V poli **Platební podmínky** v části **Ceny a slevy** vyberte platební podmínku. Více informací o **Platebních podmínkách** najdete v článku [Definování platebních podmínek dodavatelů](../accounts-payable/tasks/define-vendor-payment-terms.md). 
2. Vyberte platební podmínku, která má na stránce **Platební podmínky** vybranou možnost **Od držitele zálohy**. 
3. Na záložce **Ceny a slevy** v poli **Držitel zálohy** vyberte držitele zálohy pro nákupní objednávku.

Proces zaúčtování nákupní objednávky vytvoří dvě transakce dodavatele s opačným částkami a jednu transakci držitele zálohy. Bez podrobností držitele zálohy je vytvořena pouze jedna transakce dodavatele.

### <a name="settle-advance-holder-balances-by-using-the-bank"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím banky
Když vyrovnáte zůstatky držitelů záloh prostřednictvím banky, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v hlavním deníku. Můžete nastavit kód pro deník a banky v části **Držitelé záloh** na stránce **Parametry závazků**. 

1. Pro uzavření zůstatku držitele zálohy prostřednictvím banky, přejděte do nabídky **Závazky** > **Držitelé záloh** > **Držitelé záloh**. 
2. V podokně akcí vyberte **Zůstatek** > **Uzavřít v bance**. 
3. Na stránce **Uzavřít v bance** zadejte následující informace.

    | Pole                    | popis |
    |------------------------------|-------------------|
    | **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
    | **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** na stránce **Zůstatek**, je ve výchozím nastavení zobrazena. |
    | **Automatické**                | Vyberte zaškrtávací políčko **Automaticky** pro automatické vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.|

### <a name="settle-advance-holder-balances-by-using-cash"></a>Vyrovnání zůstatků držitele zálohy prostřednictvím hotovosti
Když vyrovnáte zůstatky držitelů záloh prostřednictvím hotovosti, položky deníku pro uzavření zůstatků držitele zálohy jsou vytvořeny v deníku dokladů. Můžete nastavit kód pro deník a hotovost na kartě **Držitelé záloh** na stránce **Parametry závazků**. 

1. Pro uzavření zůstatku držitele zálohy prostřednictvím hotovosti, přejděte do nabídky **Závazky** > **Držitelé záloh** > **Držitelé záloh**. 
2. V podokně akcí vyberte **Zůstatek** > **Uzavřít v hotovosti**. 
3. Na stránce **Uzavřít v hotovosti** zadejte následující informace.

    | Pole                    | popis
    |------------------------------|-----------------|
    | **Datum platby**          | Zadejte datum, ke kterému má být platba zaúčtována.|
    | **Převáděná částka** | Zadejte částku zůstatku při zavírání. Částka, která je uvedena v poli **Částka** na stránce **Zůstatek**, je ve výchozím nastavení zobrazena. |
    | **Automatické**                | Vyberte zaškrtávací políčko **Automaticky** pro automatické vytvoření a zaúčtování deníku, který je přednastavený na stránce **Parametry závazků**.     |

Po zpracování deníku dokladů, pokud částka v poli **Převáděná částka** je záporná, výdajový doklad je vygenerován pro držitele zálohy při uzavření zůstatků. Pokud částka v poli **Převáděná částka** byla pozitivní, vygeneruje se refundační doklad.

## <a name="additional-resources"></a>Další zdroje

- [Záloha pro zaměstnance (východní Evropa)](tasks/advance-payment-employee.md)
- [Přehled držitelů záloh pro Rusko](rus-advance-holders.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
