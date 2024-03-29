---
title: Konfigurace polí pro mobilní aplikaci Warehouse Management
description: Tento článek popisuje, jak definovat a konfigurovat názvy a priority polí v mobilní aplikaci Řízení skladu.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00a20faaa05a9d0891ee202951b1ca50d0176c83
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065951"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Konfigurace polí pro mobilní aplikaci Warehouse Management

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak definovat a konfigurovat názvy a priority polí v mobilní aplikaci Řízení skladu.

> [!NOTE]
> Tento článek se vztahuje k funkcím v modulu Řízení skladu. Nevztahuje se na funkce v modulu Řízení zásob. Mobilní aplikace Řízení skladu je aplikace, která slouží k provádění úloh skladu. Je možné definovat a konfigurovat názvy polí použitých v aplikaci, jakož i konfigurovat priority, do kterých by měly být přiřazeny názvy polí. Tento článek vysvětluje, jak definovat a konfigurovat tyto názvy a priority polí mobilní aplikace Řízení skladu, a zároveň způsob jejich použití.

## <a name="configure-warehouse-app-field-names"></a>Konfigurace názvů polí aplikace skladu

Použijete-li aplikaci Warehousing na svém mobilním zařízení, můžete nakonfigurovat, jakým způsobem se zobrazí metadata na vašem zařízení na stránce **Názvy polí aplikace skladu**. V nové společnosti vyberte možnost **Vytvořit výchozí nastavení** pro vygenerování názvů všech polí, které budou použity ve workflow skladu na mobilním zařízení, přiřaďte jim upřednostňovaný vstupní režim a typ vstupu. Po vygenerování všech názvů polí můžete vybrat následující možnosti vstupu.

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
<td>Tato možnost určuje, zda se mají pro zvolený název pole zobrazovat prohledávací pole nebo vstupní pole ručního zadávání. To je užitečné k rozlišení polí v závislosti na tom, zda se používají pro pole čárové kódy. <strong>Poznámka:</strong> Pro názvy polí s upřednostňovaným vstupním režimem nastaveným na <strong>Vyhledávání</strong> můžete zadat informace ručně, pokud není čárový kód čitelný nebo je poškozen.</td>
</tr>
<tr class="even">
<td>Vstupní typ</td>
<td>Tato možnost určuje, jaký typ vstupu má být použit pro název vybraného pole. K dispozici jsou čtyři možnosti:
<ul>
<li><strong>Výběr </strong> - Obsahuje seznam možností k výběru. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Datum</strong> - Názvy polí specifikované jako datum zobrazí formát data s popiskem. To pomáhá pracovníkům skladu zjistit, v jakém formátu zadat datum. Názvy polí s touto možností nejsou upravitelné.</li>
<li><strong>Alfa</strong> - Je-li tato možnost vybrána, použije se při ručním zadávání informací do aplikace klávesnice zařízení. Vlastnosti klávesnice lze změnit podle toho, na kterém zařízení se používá.</li>
<li><strong>Číselný</strong> - Pro názvy polí používající pouze číselné vstupy můžete vybrat tuto možnost, chcete-li zobrazit vlastní numerickou klávesnici s vstupní polem místo klávesnice zařízení.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Konfigurace priority pole aplikace skladu

Na stránce **Priorita pole aplikace skladu** můžete umístit názvy polí do různých skupin priority. Díky tomu je možné se rozhodnout, jaké informace mají být zobrazeny na hlavní stránce úloh, když pracovníci skladu provádět úlohy pomocí této aplikace. Pokud klikněte na možnost **Vytvořit výchozí nastavení**, vygeneruje se výchozí sada skupin priority. Je možné vytvořit libovolný počet skupin priority podle potřeby, ale pouze tři skupiny priorit se zobrazí na stránce úloh. Když systém odesílá metadata do aplikace, přiřadí každému poli relativní prioritu v závislosti na skupině priority, a aplikace zobrazí první tři skupiny priority obsažené v metadatech na stránce úloh. Zbývající metadata se zobrazí na sekundární stránce podrobností. V následující tabulce je uveden příklad pěti skupin priority.

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

Například pokud pracovník skladu provádí úlohu na mobilním zařízení, skutečnost, zda se metadata zobrazí v aplikaci, se skládá z následujících polí:

-   Zboží
-   Množství
-   Měrná jednotka
-   Popis položky
-   Velikost a umístění

Na základě nastavení priority pole aplikace skladu ve výše uvedené tabulce se zobrazí na stránce úloh následující 3 řádky informací:

-   Řádek 1: Položka, množství a měrná jednotka
-   Řádek 2: Popis položky
-   Řádek 3: Velikost

Zbývající metadata, například umístění, se nezobrazí na stránce úloh, ale budou zobrazena na stránce podrobností. Další informace a příklady uživatelského rozhraní naleznete v příspěvku blogu [Oznámení aplikace Dynamics 365 Supply Chain Management - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Další prostředky

[Instalace a připojení mobilní aplikace Řízení skladu](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
