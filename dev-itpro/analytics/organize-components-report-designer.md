---
title: "Uspořádání součástí zprávy v návrháři sestavy"
description: "Poté, co jste navrhli stavební bloky a vygenerovali sestavy, je užitečné uspořádat tyto objekty a usnadnit uživatelům jejich vyhledání. Tento článek popisuje způsob uspořádání existujících sestav, stavebních bloků a objektů v návrháři sestav."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 19 - 06 - 25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: c8efd57805cd89eb8cdfabe81a60704bb4390194
ms.lasthandoff: 03/29/2017


---

# <a name="organize-report-components-in-report-designer"></a>Uspořádání součástí zprávy v návrháři sestavy

Poté, co jste navrhli stavební bloky a vygenerovali sestavy, je užitečné uspořádat tyto objekty a usnadnit uživatelům jejich vyhledání. Tento článek popisuje způsob uspořádání existujících sestav, stavebních bloků a objektů v návrháři sestav.

Můžete přejmenovat složky, sestavy, stavební bloky a jiné objekty v návrháři sestavy k usnadnění uspořádání souborů. V závislosti na typu objekt, jehož název měníte, může být nutné aktualizovat přidružení tohoto objektu.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Přejmenování složky nebo stavebního bloku v Návrháři sestav
V Návrháři sestav můžete přejmenovat složky, definice sestav, definice řádků, definice sloupců a definice stromu výkaznictví. **Poznámka:** při přejmenování stavebního bloku je nutné aktualizovat všechny definice sestavy, které používají daný stavební blok. Jinak nelze vytvořit novou sestavu.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Přejmenování složky nebo stavebního bloku v Návrháři sestav

1.  V Návrháři sestav můžete k vyhledání složky nebo objektu k přejmenování použít navigační podokno.
2.  Klikněte pravým tlačítkem myši na objekt a poté klikněte na možnost **Přejmenovat**. Pole **Název** v podokně navigace se zpřístupní.
3.  Zadejte nový název a stiskněte klávesu Enter.
4.  Pokud je stavební blok definicí řádku, definicí sloupce nebo definicí stromu výkaznictví, je nutné aktualizovat další stavební bloky, které jsou k němu přidružené. Klikněte pravým tlačítkem myši na stavební blok, který jste přejmenovali v kroku 3, vyberte položku **Přidružení** a poté vyberte položku v seznamu k aktualizaci.
5.  Opakujte krok 4, dokud nebudou aktualizovány všechny přidružené položky.

## <a name="create-and-manage-report-groups"></a>Vytvoření a správa skupin sestav
Můžete seskupovat definice sestavy a generovat více sestav současně. Abyste mohli vytvářet, upravovat, odstraňovat a generovat skupiny sestav, musíte mít roli návrháře nebo správce. Uživatelé s rolí generátora mohou generovat skupiny sestav a mohou také upravovat nastavení definic sestavy pro skupiny sestav.

### <a name="create-a-report-group"></a>Vytvoření skupiny sestav

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.
2.  V nabídce **Soubor** klepněte na **Nový** &gt; **Definice skupiny sestav** a otevřete tak novou skupinu sestav v okně prohlížeče. Případně klikněte na tlačítko **Skupina sestav** ![Skupina sestav](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Skupina sestav") na panelu nástrojů.
3.  Klikněte na kartu Seskupit podle **Skupina sestav**. Pro přepsání informací v jednotlivých definicích sestavy pro generování této sestavy zaškrtněte políčko **Přepsat nastavení společnosti, podrobností a data z jednotlivých definic sestavy**. Název společnosti, úroveň podrobností, nastavení předběžných údajů a datum jsou vyplněny automaticky, ale přesto můžete provést aktualizaci.
4.  Zaškrtněte políčko **Zahrnout všechny měny vykazování**, pokud chcete vygenerovat více sestav zobrazujících tyto měny. Více zobrazení pak bude k dispozici po kliknutí na tlačítko **Měna** ve Webovém prohlížeči při zobrazení sestavy.
5.  V poli **Sestavy ve skupině** kliknutím na tlačítko **Přidat** vyberte sestavy, které chcete zahrnout do skupiny sestav. Chcete-li vybrat více sestav v dialogovém okně **Přidat**, podržte klávesu Ctrl při výběru sestav. Po dokončení výběru sestav klepněte na tlačítko **OK**.
6.  Kliknutím na položky **Soubor** &gt; **Uložit** uložte novou skupinu sestav.

### <a name="modify-a-report-group"></a>Úprava skupiny sestav

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.
2.  Klikněte dvakrát na skupinu zásad, kterou chcete upravit.
3.  Klikněte na kartu **Skupina sestav** a proveďte požadované změny.
4.  V nabídce **Soubor** klikněte na příkaz **Uložit** pro uložení změněné skupiny sestav. Případně klikněte na tlačítko **Uložit** ![Uložit](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Uložit") na panelu nástrojů.

**Poznámka:** Pokud jste naplánovali sestavy tak, aby byly generovány v určitých intervalech, můžete přepsat tato nastavení a vygenerovat sestavu okamžitě.

### <a name="generate-a-report-group-report"></a>Vygenerování sestavy skupiny sestav

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.
2.  Otevřete skupinu sestav k vygenerování.
3.  Klikněte na tlačítko **Generovat sestavu** ![Generovat sestavu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generovat sestavu") pro generování sestav.

### <a name="delete-a-report-group"></a>Odstranění skupiny sestav

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.
2.  Klikněte pravým tlačítkem myši na skupinu sestav, kterou chcete odstranit, a vyberte možnost **Odstranit**.
3.  Když se zobrazí potvrzující zpráva, klepněte na tlačítko **Ano**.

## <a name="report-group-tab-controls"></a>Ovládací prvky karta Skupina sestav
Následující tabulka popisuje ovládací prvky na kartě **Skupina sestav**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kontrola</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přepsat nastavení společnosti, podrobností a data z jednotlivých definic sestavy</td>
<td>Zaškrtnutím tohoto políčka můžete přepsat jednotlivé definice sestav v této skupině sestav pro generování pouze těchto sestav.</td>
</tr>
<tr class="even">
<td>Název společnosti</td>
<td>Vyberte společnost, která má být použita pro sestavy.</td>
</tr>
<tr class="odd">
<td>Úroveň podrobností</td>
<td>Vyberte úroveň detailu, které mají sestavy obsahovat.
<ul>
<li><strong>Finanční</strong> − souhrnná sestava na vysoké úrovni. Nelze podrobně zobrazit účty a dimenze, s výjimkou účtů a dimenzí přidaných prostřednictvím stromu výkaznictví.</li>
<li><strong>Finanční &amp; účetní</strong> − sestava, která obsahuje souhrn na vysoké úrovni a podrobnosti účtu.</li>
<li><strong>Finanční, účetní &amp; transakční</strong> − sestava, která obsahuje souhrn na vysoké úrovni a podrobnosti transakcí.</li>
</ul></td>
</tr>
<tr class="even">
<td>Provizorní</td>
<td>Vyberte typy aktivit, které mají sestavy obsahovat.
<ul>
<li><strong>Pouze zaúčtované aktivity</strong> − obsahuje pouze transakce a zůstatky, které jsou zaúčtovány ve finančních datech.</li>
<li><strong>Zaúčtované i nezaúčtované aktivity</strong> − obsahuje všechny transakce a zůstatky, které jsou zadány a zaúčtovány ve finančních datech.</li>
<li><strong>Pouze nezaúčtované aktivity</strong> − obsahuje pouze transakce a zůstatky, které jsou zadané, ale zatím nejsou zaúčtované ve finančních datech.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zahrnout všechny měny vykazování</td>
<td>Pokud jsou ve vašem systému Microsoft Dynamics ERP definovány další měny vykazování, budou uvedeny zde. Označením tohoto pole vygenerujete další sestavy ve vybraných měnách. Pokud chcete tyto sestavy zobrazit ve webovém prohlížeči, klikněte na tlačítko <strong>Měna</strong> a vyberte měnu.</td>
</tr>
<tr class="even">
<td>Informace o datu nejsou uloženy s definicí sestavy</td>
<td><ul>
<li>Základní období</li>
<li>Základní rok</li>
<li>Pokryté období</li>
</ul>
Pouze výchozí nastavení základního období se uloží s definicí sestavy.</td>
</tr>
<tr class="odd">
<td>Informace o datu jsou uloženy s definicí sestavy</td>
<td><ul>
<li>Datum sestavy</li>
<li>Výchozí základní období</li>
</ul></td>
</tr>
<tr class="even">
<td>Sestavy ve skupině</td>
<td>Umožňuje přidat, odstranit a změnit pořadí sestav ve skupině sestav.
<ul>
<li>Chcete-li přidat definice sestav do skupiny sestav, kliknutím dvakrát skupinu sestav otevřete a klikněte na tlačítko <strong>Přidat</strong>. Vyberte sestavy k zahrnutí do skupiny sestav a klikněte na tlačítko <strong>OK</strong>.</li>
<li>Chcete-li odebrat sestavu ze skupiny sestav, vyberte ji a klikněte na tlačítko <strong>Odebrat</strong>.</li>
<li>Chcete-li změnit pořadí, ve kterém jsou generovány sestavy, vyberte v seznamu sestavu a klikněte na tlačítko <strong>Přesunout nahoru</strong> nebo <strong>Přesunout dolů</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví v aplikaci Microsoft Dynamics 365 for Operations](financial-reporting-intro.md)

