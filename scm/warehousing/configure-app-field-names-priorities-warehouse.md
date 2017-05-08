---
title: "Konfigurace názvů polí aplikace v aplikaci Warehousing"
description: "Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Dynamics 365 for Operations."
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

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurace názvů polí aplikace v aplikaci Warehousing

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak definovat a konfigurovat názvy polí aplikace skladu a priority v aplikaci Dynamics 365 for Operations. 

**Poznámka:** Toto téma se vztahuje k funkcím v modulu Řízení skladu. Nevztahuje se na funkce v modulu Řízení zásob. Dynamics 365 for Operations - Warehousing je aplikace, která slouží k provádění úloh skladu. Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí. Toto téma vysvětluje, jak definovat a konfigurovat tyto názvy polí aplikace skladu a priority, a zároveň způsob jejich použití v aplikaci Dynamics 365 for Operations - Warehousing. Podrobné informace o konfiguraci připojení k aplikaci Dynamics 365 for Operations - Warehousing naleznete v kurzu [Instalace a konfigurace aplikace Dynamics 365 for Operations - Warehousing](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurace názvů polí aplikace skladu
===================================

Použijete-li aplikaci Dynamics 365 for Operations - Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**. V nové společnosti v aplikaci Dynamics 365 for Operations vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu. Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.

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
<td>Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání. To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy. <strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</td>
</tr>
<tr class="even">
<td>Vstupní typ</td>
<td>Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole. K dispozici jsou čtyři možnosti:
<ul>
<li><strong>Výběr</strong> - obsahuje seznam možností k výběru. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Datum</strong> - názvy polí specifikované jako datum zobrazí formát data s popiskem. To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Alfa</strong> - -je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení. Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</li>
<li><strong>Číselný</strong> - pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurace priority pole aplikace skladu
======================================

Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority. Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace. Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority. Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh. Když odesílá aplikace Dynamics 365 for Operations metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh. Zbývající metadata se zobrazí na sekundární stránce podrobností. V následující tabulce je uveden příklad pěti skupin priority.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skupina priority</th>
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
<td> Priorita 20</td>
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
<td> Priorita 50</td>
<td><ul>
<li>Skl. místo</li>
<li>Poznávací značka</li>
</ul></td>
</tr>
</tbody>
</table>

Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:

-   Zboží
-   Množství
-   Měrná jednotka
-   Popis položky
-   Velikost a umístění

Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:

-   Řádek 1: Položka, množství a měrná jednotka
-   Řádek 2: Popis položky
-   Řádek 3: Velikost

Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností. Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Dynamics 365 for Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Viz také
--------

[Instalace a konfigurace aplikace Microsoft Dynamics 365 for Operations – Warehousing](install-configure-warehousing-app.md)



