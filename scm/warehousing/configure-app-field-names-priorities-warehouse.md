---
title: "Konfigurovat názvy polí aplikace v app týkající se skladování."
description: "Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace sklad a priority v 365 Dynamics pro operace."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurovat názvy polí aplikace v app týkající se skladování.

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace sklad a priority v 365 Dynamics pro operace. 

**Poznámka:** Toto téma se týká funkcí správy skladu. Nevztahuje se na funkce v modulu Řízení zásob. Dynamics 365 pro operace - skladování je aplikace, která slouží k provádění úloh skladu. Je možné definovat a konfigurovat názvy polí, které jsou použity v aplikace, jakož i Konfigurace priority, které by měly být přiřazeny názvy polí. Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy polí aplikace sklad a priority a jejich použití v Dynamics 365 pro operace - skladování. Podrobné informace o konfiguraci připojení k 365 Dynamics pro operace - skladování, naleznete v kurzu [instalace a konfigurace Dynamics 365 pro operace - skladování](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurace skladu názvy polí aplikace
===================================

Použijete-li pro operace - Dynamics 365 uskladnění v mobilním zařízení, můžete nakonfigurovat, jak metadat mají být zobrazeny na zařízení na **skladu názvy polí aplikace** stránky. V nové společnosti v 365 Dynamics pro operace, vyberte **vytvořit výchozí nastavení** generovat názvy všech polí, které budou použity v pracovních postupech mobilní zařízení skladu a přiřadit k nim upřednostňované vstupní režim a typ vstupu. Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametr</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Upřednostňovaný režim vstupu</td>
<td>Tato možnost určuje, zda pole vyhledávání nebo ruční zadání vstupního pole se uvede název vybraného pole. To je užitečné rozlišit pole v závislosti na Pokud čárové kódy se používají pro pole. <strong>Poznámka:</strong> pro názvy polí upřednostňovaný vstupní režim nastaven na <strong>vyhledávání</strong>, můžete zadat informace ručně Pokud je čárový kód není čitelný nebo je poškozen.</td>
</tr>
<tr class="even">
<td>Vstupní typ</td>
<td>Tato možnost určuje, jaké vstupní typ má být použit pro název vybraného pole. K dispozici jsou čtyři možnosti:
<ul>
<li><strong>Výběr</strong> - obsahuje seznam možností na výběr. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Datum</strong> - specifikované datum, zobrazí se formát data s popiskem názvů polí. To pomáhá pracovníkům skladu najdete v jakém formátu zadat datum. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Alfa</strong> - -li zaškrtnuto, zařízení klávesnice bude použita při ručním zadáním informací do aplikace. Zkušenosti klávesnice lze změnit podle toho, které zařízení používá.</li>
<li><strong>Numerická</strong> - pro dané použití numerické vstup pouze názvy polí, můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní pole místo klávesnice zařízení.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurace priority pole sklad app
======================================

Na **sklad pole Priorita app** stránky, názvy polí můžete umístit do skupin různé priority. Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na stránce hlavní úkol, když pracovníci skladu provádět úkoly pomocí aplikace. Pokud klepnete na tlačítko **vytvořit výchozí nastavení**, bude vytvořen výchozí sadu přednostních skupin. Je možné vytvořit libovolný počet přednostních skupin podle potřeby, ale pouze tři priority skupiny se zobrazí na stránce úkolu. Při 365 Dynamics pro operace odešle aplikaci metadata, přiřadí každému poli relativní prioritu podle jeho priority skupiny a aplikace se zobrazí první tři prioritní skupiny obsažené v metadatech na stránce úkolu. Na stránce sekundární podrobnosti se zobrazí zbývající přetékající metadat. V následující tabulce je uveden příklad pěti přednostních skupin.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Priority skupiny</th>
<th>Přiřazená pole</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Priorita 10</td>
<td><ul>
<li>Zboží</li>
<li>Množství</li>
<li>Měrná jednotka</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritu 20</td>
<td><ul>
<li>Pozice seskupení</li>
<li>Seskupení</li>
</ul></td>
</tr>
<tr class="odd">
<td> Priorita 30</td>
<td><ul>
<li>Popis položky</li>
</ul></td>
</tr>
<tr class="even">
<td> Priorita 40</td>
<td><ul>
<li>Konfigurace</li>
<li>Barva</li>
<li>Velikost</li>
<li>Styl</li>
</ul></td>
</tr>
<tr class="odd">
<td> Priority 50</td>
<td><ul>
<li>Skl. místo</li>
<li>Poznávací značka</li>
</ul></td>
</tr>
</tbody>
</table>

Například pokud pracovník skladu provádí úlohy v mobilním zařízení, pokud metadata, která se zobrazí v aplikace se skládá z následujících polí:

-   Zboží
-   Množství
-   Měrná jednotka
-   Popis položky
-   Velikost a umístění

Na základě skladu app pole priority nastavené v tabulce výše, následující 3 řady informace budou zobrazeny na stránce úkolu:

-   Řádek 1: Měrnou jednotku zboží, množství,
-   Řádku 2: Popis položky
-   Řádek 3: velikost

Zbývající metadata, například umístění se nezobrazí na stránce úlohy, ale bude zobrazen na stránce podrobností. Další informace a příklady uživatelského rozhraní, naleznete v příspěvku blogu [oznamující 365 Dynamics pro operace - skladování](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Viz také
--------

[Nainstalujte a nakonfigurujte Microsoft Dynamics 365 pro operace – skladování](install-configure-warehousing-app.md)




