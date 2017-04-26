---
title: "Nastavení komponent úlohy"
description: "Toto téma popisuje rámcové prvky, že úloha může obsahovat a obsahuje příklady použití těchto prvků v organizaci."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Nastavení komponent úlohy

[!include[banner](includes/banner.md)]


Toto téma popisuje rámcové prvky, že úloha může obsahovat a obsahuje příklady použití těchto prvků v organizaci. 

Před vytvořením úlohy, musíte nastavit některé referenční informace. Můžete vytvořit úlohu, která má pouze název. Však zahrnutím dalších informací, například název projektu, můžete zadat výchozí hodnoty pro pozice, které jsou přiřazeny k projektu. Navíc některé informace, které zadáte můžete použít k filtrování plánů vyrovnání určitých projektů. Pokud chcete nastavit nároku, který slouží k filtrování plány kompenzace na konkrétní práci, by nastavíte pracovní funkce a typy úloh před nastavit úlohy. Tím, že tyto výchozí hodnoty, které jsou k dispozici, ušetříte čas při přidávání pozic k projektu. 

Některé podrobnosti úlohy, jako je například název úlohy, typ a funkce, jsou skutečná data. Vytvořit úlohu dnes ale Nepřidávat tyto podrobnosti později a poté prohlédněte úlohy, jako je datum vytvoření, nezobrazí se tyto podrobnosti. Proto je třeba vytvořit některé referenční informace dříve, než jej vyžadují. Tímto způsobem můžete přidat informace do nové úlohy při jejich vytváření.

## <a name="job-titles"></a>Pracovní pozice
Před vytvořením úloh musíte nastavit názvy pro tyto úlohy. Pozice dědí názvy úloh z úloh, ke kterým jsou pozice přiřazeny. 

Udržovat pracovní pozice pomocí **názvy** stránky, které lze otevřít pomocí funkce Hledat. Na ** titulky ** zadejte názvy, které budete používat pro vaše projekty.

## <a name="job-types"></a>Typ úloh
Typy úloh slouží k seskupení podobných úloh do kategorií. Typy úloh nejsou povinné. Však pokud máte v úmyslu použít typy úloh při nastavování pravidel způsobilosti pro správu kompenzace, je třeba před nastavením úloh nastavit také typy úloh. Příklady typů úloh jsou na plný úvazek a částečný úvazek nebo plat a hodinové mzdy. Spravovat typy úloh pomocí **projektu typy** stránky. Na **projektu typy** stránky, zadejte název a stručný popis pro typ projektu. V **stav osvobodit** pole, vyberte jednu z následujících možností pro označení spravedlivé mzdové normy zákona (FLSA) osvobození od stavu úloh, které mají tento typ práce:

-   **Osvobození od** – úlohy jsou vyjmuty z přesčasů podle FLSA.
-   **Nevyňaté** – úlohy nejsou vyjmuty z přesčasů podle FLSA.
-   **Nelze použít** – pokrytí FLSA není použitelná.

## <a name="job-functions"></a>Pracovní funkce
Úloha křižovatkách popisují vysoké úrovni funkčních kategorií a vysoké úrovně cla vztahují. Pracovní funkce nejsou povinné. Pracovní funkce a typy úloh, můžete použít k filtrování plánů vyrovnání určitých projektů. Můžete přidružit pracovní funkce a typy úloh plány kompenzace nastavením pravidel způsobilosti na **pravidla způsobilosti** stránky. Sada úrovní lze potom připojit k plánu kompenzace, který platí pro určité kombinace typu úlohy a pracovní funkce, kterou jste definovali pomocí pravidlo způsobilosti. (Tyto funkce lze použít pro plány fixní kompenzace a plány variabilní kompenzace.) Nicméně pokud plánujete použít funkci při nastavování pravidel způsobilosti pro správu kompenzace, by nastavíte pracovní funkce před nastavit úlohy. V následující tabulce jsou uvedeny příklady pracovních funkcí.

| Práce           | Pracovní funkce         |
|---------------|----------------------|
| Manažer prodeje | Správce střední úrovně    |
| Účetní    | Odborníci v oblasti IT        |

Udržovat pracovní funkce pomocí **funkcí úkolu** stránky. Na **funkcí úkolu** zadejte identifikační kód a stručný popis pracovní funkce.

## <a name="job-tasks"></a>Pracovní úkoly
Úlohy jsou popsány základní úlohy, které musí pracovník, který je v pozici pro práci dokončit. Stejnou úlohu lze přidat více úloh a pozic pro úlohy, které používají tyto úlohy. V následující tabulce jsou uvedeny příklady úkolů.

<table>
<thead>
<tr class="header">
<th>Práce</th>
<th>Pracovní úkol</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Manažer prodeje</td>
<td><ul>
<li><strong>Přezkoumání perf</strong> – zkontrolovat výkon každého prodejce projektu.</li>
<li><strong>Přezkoumání Abs</strong> – schválit nebo odmítnout požadavky absencí nebo registrace každého prodejce.</li>
</ul></td>
</tr>
<tr class="even">
<td>Účetní</td>
<td><strong>Zpráva FIN</strong> – týdenní finanční výkazy předložit finanční ředitel.</td>
</tr>
</tbody>
</table>

Spravovat úlohy pomocí **úlohy** stránky. Na **úlohy** stránky, zadejte název a popis úlohy. V **Poznámka:** pole, můžete volitelně zadat další informace. Poznámky mohou být aktualizovány na určitém projektu beze změny poznámky, které jste zadali v tomto poli.

## <a name="areas-of-responsibility"></a>Oblasti odpovědnosti
Oblasti odpovědnosti slouží k určení pracovní role, procesy a produkty, které je zodpovědný za pracovníka, který je v umístění pro projekt. Pro úlohu s názvem "Účetní", například jednu oblast odpovědnosti může být "Finanční vykazování pro produkt A." Můžete udržovat pomocí oblasti odpovědnosti **oblasti odpovědnosti** stránky, které lze vyhledat pomocí funkce Hledat. Na **oblasti odpovědnosti** stránky, zadejte název a popis pro odpovědnost. V **Poznámka:** pole, můžete volitelně zadat další informace. Poznámky mohou být aktualizovány na určitém projektu beze změny poznámky, které jste zadali v tomto poli.




