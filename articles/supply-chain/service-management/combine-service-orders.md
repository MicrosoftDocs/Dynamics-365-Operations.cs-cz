---
title: Kombinace servisních zakázek
description: Servisní zakázky můžete kombinovat.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676768"
---
# <a name="combine-service-orders"></a>Kombinace servisních zakázek   

[!include [banner](../includes/banner.md)]


Při vytváření řádků servisní zakázky automaticky ve formuláři **servisní smlouvy** můžete vybrat některou z následujících možností k určení způsobu jejich seskupení:

  - **Podle servisní smlouvy**

  - **Podle servisní úlohy**

  - **Podle zaměstnance**

  - **Podle předmětu servisu**

## <a name="example"></a>Příklad

Vytvoříte servisní smlouvu s počátečním datem 31. 3. 2007. V poli **Kombinace servisních zakázek** vyberte **Podle předmětu servisu**. Poté vytvoříte následující řádky servisní zakázky:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Číslo řádku smlouvy</p></th>
<th><p>typ transakce</p></th>
<th><p>popis</p></th>
<th><p>Interval</p></th>
<th><p>Předmět servisu</p></th>
<th><p>Datum zahájení</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Hodina</strong></p></td>
<td><p>ŘSZ1</p></td>
<td><p>Týdně</p></td>
<td><p>X-1</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Hodina</strong></p></td>
<td><p>ŘSZ2</p></td>
<td><p>Každé 2 týdny</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Hodina</strong></p></td>
<td><p>ŘSZ3</p></td>
<td><p>Týdně</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
</tbody>
</table>


Pro žádný z řádků servisní zakázky nevytvoříte časová okna. Řádky servisní zakázky proto nebude možné přesunout z vypočteného data, na které připadají.

Poté vygenerujete řádky servisní zakázky z formuláře **Vytvořit servisní zakázky** od 01.04.2007 do 30.04.2007.

Celkem vytvoříte 10 servisních zakázek. Vzhledem k tomu, že jste vybrali nastavení kombinace **Podle předmětu servisu**, budou všechny vytvořené servisní zakázky obsahovat pouze řádky servisní zakázky, které se vztahují k jednomu konkrétnímu předmětu servisu. Do jedné servisní zakázky budou zkombinovány řádky servisní zakázky vygenerované ze servisní smlouvy, které mají stejné datum servisu a stejný předmět.


> [!NOTE]
> <P>V tomto příkladu neobsahuje kalendář uvedený ve formuláři <STRONG>Parametry řízení servisu</STRONG> žádné uzavřené dny.</P>



Další seskupení řádků servisní zakázky do servisních objednávek vychází z časového intervalu, který jste zadali na řádcích servisní zakázky.

## <a name="see-also"></a>Viz také

[Automatické vytvoření servisních zakázek](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]