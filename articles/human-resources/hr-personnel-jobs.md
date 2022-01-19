---
title: Nastavení komponent práce
description: Toto téma popisuje rámcové prvky, které může práce obsahovat, a poskytuje příklady použití těchto prvků v organizaci.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4aa7369c84836154b8217a5b70267021f4028b1
ms.sourcegitcommit: 4f84540e6121ca3d5ae52ee07e414116d423cefa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/03/2022
ms.locfileid: "7948468"
---
# <a name="set-up-the-components-of-a-job"></a>Nastavení komponent práce

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje rámcové prvky, které může práce obsahovat, a poskytuje příklady použití těchto prvků v organizaci. 

Než budete moci vytvořit práce, musíte nastavit některé referenční informace. Můžete vytvořit práci, která má pouze název. Když však zahrnete další informace, například název pracovní pozice, poskytnete výchozí hodnoty pozice, které jsou přiřazeny k práci. Navíc některé informace, které zadáte, mohou být použity k filtrování plánů kompenzací pro konkrétní práce. Pokud chcete nastavit nárok, který slouží k filtrování plánů kompenzace pro konkrétní práci, měli byste nastavit pracovní funkce a typy prací předtím, než nastavíte práce. Tím, že tyto výchozí hodnoty budete mít k dispozici, ušetříte čas při přidávání pozic k práci. 

Některé podrobnosti o práci, jako je například název pracovní pozice, typ a funkce, platí od data zadání. Pokud vytvoříte práci dnes a přidáte tyto podrobnosti až později, tyto podrobnosti se nezobrazí, když si zobrazíte práci k datu jejího vytvoření. Proto je třeba vytvořit některé referenční informace dříve, než je budete potřebovat. Tímto způsobem můžete přidat informace do nových prací při jejich vytváření.

## <a name="job-titles"></a>Názvy pracovních pozic
Před vytvořením úloh musíte nastavit názvy pro tyto úlohy. Pozice dědí názvy úloh z úloh, ke kterým jsou pozice přiřazeny. 

Udržujte názvy pracovních pozic pomocí stránky **Pozice**, kterou lze otevřít pomocí funkce hledání. Na stránce **Pozice** zadejte názvy, které budete používat pro vaše práce.

## <a name="job-types"></a>Typy práce
Používáte typy prací pro seskupení podobných pozic do kategorií. Typy práce nejsou vyžadovány. Však pokud máte v úmyslu použít typy úloh při nastavování pravidel způsobilosti pro správu kompenzace, je třeba před nastavením úloh nastavit také typy úloh. Některé příklady typů prací jsou na plný úvazek a částečný úvazek, nebo plat a hodinové mzda. Typy práce udržujte pomocí stránky **Typy práce**. Zadejte název a stručný popis typu pozice na stránce **Typy práce**. V poli **Stav osvobození** vyberte jednu z následujících možností pro označení stavu osvobození od zákona Fair Labor Standards Act (FLSA) pro práce, které mají tento typ práce:

-   **Osvobozené** – Práce jsou vyjmuty z přesčasů podle zákona FLSA.
-   **Neosvobozené** – Práce nejsou vyjmuty z přesčasů podle zákona FLSA.
-   **Nelze použít** – pokrytí zákonem FLSA není možné.

## <a name="job-family"></a>Skupina pracovních míst
Skupina pracovních míst je skupina prací, které zahrnují podobnou práci a které vyžadují podobné školení, dovednosti, znalosti a odborné znalosti. Rodina pracovních míst může být spojena s pozicí na pevné záložce **Pracovní zařazení** stránky **Pracovní místa** a na pevné záložce **Všeobecné** stránky **Všechny pozice**. Rodiny pracovních pozic mohou být široké nebo konkrétní, v závislosti na vašem podnikání a požadavcích na podávání zpráv. Některé příklady širokých rodin pracovních pozic jsou **Kvalifikovaná práce** a **Nekvalifikovaná práce**. Některé příklady konkrétních rodin pracovních pozic jsou **Účetnictví**, **Výroba** a **Prodej**.

Udržujte rodiny pracovních pozic pomocí stránky **Rodina pracovních pozic**, kterou lze otevřít pomocí funkce hledání. Na stránce **Rodina pracovních pozic** zadejte jedinečný název rodiny a zadejte podrobný popis, který chcete použít pro své úlohy.

## <a name="job-functions"></a>Pracovní funkce
Křižovatky prací popisují funkční kategorie vysoké úrovně a vztahují se k povinnostem vysoké úrovně. Pracovní funkce nejsou vyžadovány. Pracovní funkce můžete používat spolu s typy práce k filtrování plánů kompenzace pro konkrétní práce. Přiřazení pracovních funkcí a typů práce k plánům kompenzace se provádí nastavením pravidel nároku na stránce **Pravidla způsobilosti**. K plánu kompenzace lze také přiřadit sadu úrovní, které se uplatní pro určité kombinace typu úlohy a pracovní funkce, které jste definovali v pravidlu nároku. (Tyto funkce platí jak pro fixní, tak pro variabilní kompenzační plány.) Pokud však chcete použít pracovní funkce při nastavování pravidel nároku pro správu kompenzací, doporučujeme nastavit pracovní funkce ještě před nastavením prací. V následující tabulce jsou uvedeny některé příklady pracovních funkcí.

| Práce           | Pracovní funkce         |
|---------------|----------------------|
| Manažer prodeje | Manažer střední úrovně    |
| Účetní    | Profesionálové        |

Pracovní funkce udržujte pomocí stránky **Pracovní funkce**. Zadejte identifikační kód a stručný popis pro pracovní funkci **Pracovní funkce**.

## <a name="compensation"></a>Kompenzace
Chcete-li přiřadit plán pevné kompenzace zaměstnanci, který má pozici v práci, musíte v práci nastavit úrovně odměny. **Úroveň kompenzace** se používá, když jsou ve struktuře kompenzace (mřížka kompenzace) nastaveny minimální, střední a maximální částky. Když je vytvořen plán pevné kompenzace, je vybrána struktura kompenzace. Struktura kompenzace také zahrnuje úroveň kompenzace. Když vybíráte plán pevné kompenzace pro zaměstnance, úrovně kompenzace, které jsou k dispozici pro výběr, závisí na úloze, se kterou je pozice zaměstnance spojena. Další informace o nastavení kompenzací naleznete v tématu [Plány kompenzace](hr-compensation-overview.md).

## <a name="job-skills"></a>Pracovní dovednosti
Pracovní dovednosti popisují dovednosti, které jsou vyžadovány k výkonu práce. S každou pracovní dovedností musí být spojena úroveň dovednosti. Úrovně dovedností jsou definovány uživatelem. Označují úroveň znalostí nebo dovedností, která je pro danou dovednost požadována. Společnosti mohou například nastavit číselné úrovně, například 1 až 5, kde **1** označuje začátečníka a **5** označuje odborníka. Alternativně mohou společnosti nastavit úrovně, které jsou označeny **Začátečník**, **Středně pokročilí** nebo **Expert**. Po nastavení úrovně dovedností lze také nastavit důležitost dovednosti. Například pokud má účetní mít silné znalosti Microsoft Excel, lze vytvořit dovednost, která je pojmenována **Znalosti aplikace Excel**. Úroveň dovednosti pak může být nastavena na **Středně pokročilý** a lze nastavit důležitost na **Většina**.

Dovednosti, které jsou v pracovní pozici, lze použít při mapování dovedností. Mapování dovedností může porovnávat sadu dovedností požadovaných pro danou práci a dovednosti spojené s pracovníkem. Poté může určit procentuální shodu na základě překrývajících se dovedností. Další informace o mapování dovedností najdete v části [Konfigurace dovedností](hr-develop-skills.md). 

## <a name="job-tasks"></a>Pracovní úkoly
Pracovní úkoly popisují základní úlohy, které musí pracovník na této pracovní pozici dokončit. Stejný pracovní úkol lze přidat do více prací a do pozic pro práce, které používají tyto pracovní úkoly. V následující tabulce jsou uvedeny některé příklady pracovních úkolů.

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
<li><strong>Zkontrolovat výkon</strong> – zkontrolování výkonu práce jednotlivých prodejců.</li>
<li><strong>Kontrola absence</strong> – schválení nebo odmítnutí požadavků nebo registrace absence jednotlivých prodejců.</li>
</ul></td>
</tr>
<tr class="even">
<td>Účetní</td>
<td><strong>Finanční sestava</strong> – předložení týdenních finančních sestav vedoucímu finančního oddělení.</td>
</tr>
</tbody>
</table>

Pracovní úkoly udržujte pomocí stránky **Pracovní úkoly**. Zadejte název a popis pracovního úkolu na stránce **Pracovní úkoly**. Do pole **Poznámka** můžete volitelně zadat další informace. Poznámky mohou být aktualizovány pro konkrétní práci beze změny poznámek, které jste v tomto poli zadali.

## <a name="areas-of-responsibility"></a>Oblasti odpovědnosti
Za pomoci oblastí odpovědnosti můžete určit pracovní role, procesy a produkty, za které je pracovník na dané pozici odpovědný. Například pro práci s názvem „Účetní“ může být oblast zodpovědnosti „Finanční výkaznictví za výrobek A“. Udržujte oblasti odpovědnosti pomocí stránky **Oblasti odpovědnosti**, kterou lze vyhledat pomocí funkce vyhledávání. Zadejte název a stručný popis odpovědnosti na stránce **Oblasti odpovědnosti**. Do pole **Poznámka** můžete volitelně zadat další informace. Poznámky mohou být aktualizovány pro konkrétní práci beze změny poznámek, které jste v tomto poli zadali.

## <a name="steps-for-creating-a-job"></a>Postup při vytváření práce
Ohledně podrobného postupu pro vytvoření nové práce nahlédněte do článku [Definování nových prací](./hr-personnel-define-jobs.md). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
