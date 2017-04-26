---
title: "Uspořádání pomocí oddělení, úlohy a pozice pracovníků"
description: "Oddělení, úlohy a pozice jsou organizační prvky, které jsou evidovány v rámci modulu Lidské zdroje. Toto téma obsahuje koncepční informace o těchto prvcích."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: f1bbc66ecefb12d14d7d707ada2b99ca42b3fdd8
ms.lasthandoff: 03/31/2017


---

# <a name="organize-your-workforce-using-departments-jobs-and-positions"></a>Uspořádání pomocí oddělení, úlohy a pozice pracovníků

[!include[banner](includes/banner.md)]


Oddělení, úlohy a pozice jsou organizační prvky, které jsou evidovány v rámci modulu Lidské zdroje. Toto téma obsahuje koncepční informace o těchto prvcích. 

Následující příklad slouží k zobrazení konceptů popsaných v tomto tématu.

|**Oddělení**|**Position**|**Job**|
|---|---|---|
|**Prodej**|Manažer prodeje (východ)|Manažer prodeje|
|**Prodej**|Manažer prodeje (západ)|Manažer prodeje|
|**Prodej**|Manažer prodeje (střed)|Manažer prodeje|
|**Accounting**|Účetní supervizor|Účetní manažer|
|**Accounting**|Účetnictví A|Účetní|
|**Human resources**|Manažer lidských zdrojů (východ)|Manažer lidských zdrojů|
|**Human resources**|Manažer lidských zdrojů (západ)|Manažer lidských zdrojů|
|**Human resources**|Manažer lidských zdrojů (střed)|Manažer lidských zdrojů|

 
 <a name="departments"></a>Oddělení
------------

Oddělení je provozní jednotka, která představuje kategorii nebo funkční oblast organizace, která je zodpovědná za určitou oblast organizace, jako například prodej nebo účtování. Oddělení slouží k hlášení ve funkčních oblastech a může mít odpovědnost za zisky a ztráty. Oddělení také mohou obsahovat i skupinu nákladových středisek. Prodej, účtování a lidské zdroje jsou některé příklady oddělení v rámci organizace.

## <a name="jobs-and-positions"></a> Úlohy a pozice
Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci. Pozice je individuální instance práce. Oblasti odpovědnosti, pracovní úkoly, pracovní funkce, dovednosti, informace o vzdělání a certifikáty, které jsou požadovány pro úlohu, jsou nutné také pro pozice, které jsou asociovány s určitou pozicí.
### <a name="job-tasks"></a>Pracovní úkoly

Můžete vytvořit pracovní úkoly, které popisují základní úlohy, které musí pracovník na pozici této úlohy dokončit. Stejnou úlohu lze přidat do více úloh a pozice pro tyto úlohy zdědí tyto úlohy. Příklady pracovních úloh jsou uvedeny v následující tabulce.

<table>
<thead>
<tr class="header">
<th>Úloha</th>
<th>Pracovní úkol</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Manažer prodeje</td>
<td><ul>
<li><span class="input">Zkontrolovat výkon</span> – zkontrolování výkonu práce jednotlivých prodejců.</li>
<li><span class="input">Kontrola absence</span> – schválení nebo odmítnutí požadavků nebo registrace absence jednotlivých prodejců.</li>
</ul></td>
</tr>
<tr class="even">
<td>Účetní</td>
<td><span class="input">Finanční sestava</span> – předložení týdenních finančních sestav vedoucímu finančního oddělení.</td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a>Pracovní funkce

Pracovní funkce jsou stejné jako pracovní úkoly. Pracovní funkce popisuje jeden nebo více úkolů, povinností nebo odpovědností, které jsou přiřazeny k práci. Pracovní funkce můžete přiřazeno projektům a slouží k nastavení a implementovat pravidla způsobilosti pro vyrovnání plány. V následující tabulce jsou uvedeny příklady pracovních funkcí.

| Úloha           | Pracovní funkce                                                |
|---------------|-------------------------------------------------------------|
| Manažer prodeje | Správa osob – správa uživatelů, kteří jsou vám podřízeni.               |
| Účetní    | Finanční kontrola – udržování finančních dat pro skupinu účtů. |

### <a name="job-types"></a>Typ úloh

Používejte typy úloh pro klasifikaci podobných pozic do kategorií. Typy úloh, jako jsou pracovní funkce, mohou být přiřazeny k pozicím a slouží k nastavení a implementaci pravidel způsobilosti pro plány kompenzace. V následujícím seznamu jsou uvedeny některé příklady typů úloh:
-   Plný úvazek
-   Částečný úvazek
-   Mzda
-   Hodinová mzda

### <a name="areas-of-responsibility"></a>Oblasti odpovědnosti

Za pomoci oblastí odpovědnosti můžete určit pracovní role, procesy a produkty, za které je pracovník na dané pozici odpovědný. příkladem oblasti odpovědnosti pro práci s názvem "Účetní" může být "Finanční vykazování pro produkt A".

<a name="positions"></a>Pozice
----------

Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace. Pozice je individuální instance práce. Například pozici "Sales manager (východ)," je pouze jedním z pozic, které jsou přidruženy k této úloze "Sales manager". Pozice v oddělení existují a jsou přiřazeny pracovníkům.
### <a name="position-creation-and-maintenance"></a>Vytváření a údržba pozic

-   Historii systémových změn pozic můžete zobrazit na snadno dostupné stránce.
-   Můžete vytvořit kódy důvodů, které mohou uživatelé vybrat při vytváření a změně pozic.
-   Můžete vytvořit typy akcí personálu a přiřadit k uživatelským akcím číselné řady.
-   Workflow lze nastavit tak, aby přidání a změny pozic bude vyžadovat schválení.

### <a name="position-duration"></a>Doba trvání pozice

Každá pozice má časový interval, kdy je pozice platná. Tento časový interval se nazývá trvání. Například můžete mít letní pozici s trváním od 1. května 2015 do 31. srpna 2015.

### <a name="worker-assignments"></a>Přiřazení pracovníků

Po přiřazení pracovníka k pozici dojde k zaplnění této pozice. Zaměstnance lze přiřadit do více pozic, ale pouze jeden pracovní může být přiřazen na pozici současně.

### <a name="reporting-relationships"></a>Vztahy sestav

Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace. Ve formuláři Pozice můžete určit pozici, která je nadřízená vaší pozici. Po přiřazení pracovníka k pozici, která je podřízena jiné pozici, můžete vytvořit vztah vykazování mezi zaměstnanci, kteří jsou přiřazeni do dvou pozic. Například pozice "Účetní A" vykazuje do pozice "Účetní supervizor" Kim Akers je přiřazen na pozici "Účetní supervizor" a Sanjay Patel je přiřazen na pozici "Účetní A". To znamená, že Sanjay Patel je podřízen uživateli Kim Akers. 

Pokud vaše společnost používá hierarchii matice nebo jinou vlastní hierarchii, můžete nastavit typy hierarchií pozic a přidat vztahy podřízenosti k pozicím pro každý nastavený typ hierarchie. Například Lori Penor je hlavní manažer společnosti Adventure Works a je přiřazený na pozici "Generální ředitel". Lori spravuje vývoj produktu, který slouží k vymazání pomůcek. Lori vyžaduje pomoc účetního s financemi pro vývoj produktu. Proto najala Sanjay Patel jako svého účetního. Sanjay je podřízen přímo pro Kim Akers, ale také pracuje s Lori Penor na jeho práci související s financemi pro vývoj produktu pro čištění pomůcek. 

V předchozím příkladu byste při nastavení pracovních vztahů mezi Sanjay Patel a Lori Penor provedli následující úkony:
1.  Vytvoření vlastního typu hierarchie pozice s názvem "Pomůcka" pro vytvoření hierarchie, která zahrnuje pozice odpovědné za práci na produktu pro čištění pomůcek.
2.  Přiřazení pozice Generální ředitel na pozici, která je nadřazena pozici Účetní A v hierarchie Pomůcka.

Použití hierarchie pozic pro zobrazení struktury hlášení pozic. Pokud máte více hierarchií pozic, můžete zobrazit hierarchii pro každý typ hierarchie v hierarchii pozic. Dále můžete vyhledávat pozici podle ID pozice nebo podle jména pracovníka, který je přiřazený na pozici. Hierarchie pozice je organizační hierarchie.

## <a name="date-effective-records"></a>Časově platné záznamy
Pro některé záznamy můžete určit budoucí změny tohoto záznamu. Následující informace jsou časově platné.

<table>
<thead>
<tr class="header">
<th>Záznamy</th>
<th>Datum platnosti pracovníka</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Práce</td>
<td><ul>
<li>Některé podrobné informace o úloze</li>
<li>Informace o klasifikaci úlohy</li>
<li>Informace o kompenzaci</li>
</ul></td>
</tr>
<tr class="even">
<td>Pozice</td>
<td><ul>
<li>Některé podrobné informace o pozici</li>
<li>Přiřazení pracovníků</li>
<li>Doby trvání pozice</li>
<li>Hierarchie pozic</li>
</ul></td>
</tr>
</tbody>
</table>

Můžete upravovat údaje uvedené v předchozí tabulce pro pozice nebo úlohy a zadat datum, kdy by se změny pozice pro vybrané úlohy měly projevit. Například pozice lze přiřadit pouze jednomu pracovníkovi, ale Sanjay Patel, který je přiřazený k pozici Účetní A odchází za dva týdny. Joe Healy nahradí Sanjay Patel po jeho odchodu. Přestože Sanjay je i nadále přiřazen na svoji pozici, můžete přiřadit Jan Healy na stejnou pozici tak, aby přiřazení nabylo platnosti až po posledním dni Sanjay.






