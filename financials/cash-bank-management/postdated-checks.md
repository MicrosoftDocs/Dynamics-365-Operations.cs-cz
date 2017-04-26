---
title: "Postdatované šeky"
description: "Tento článek obsahuje informace o podpoře pro postdatované šeky ve 365 Microsoft Dynamics pro operace. Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu. Takže lze šek proplatit až od určeného data."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Postdatované šeky

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o podpoře pro postdatované šeky ve 365 Microsoft Dynamics pro operace. Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu. Takže lze šek proplatit až od určeného data.

365 Microsoft Dynamics pro operace podporuje úplné řízení cyklu pro postdatované šeky do pohledávek a závazků, jak je znázorněno v následující tabulce.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scénář</th>
<th>Podrobnosti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nastavení postdatovaných šeků</td>
<td>Musíte nastavit novou metodu platby a zadat platební postup pro clearingové účty pro vydané šeky, přijaté šeky a srážkovou daň.</td>
</tr>
<tr class="even">
<td>Registrace a účtování postdatovaného šeku pro dodavatele</td>
<td>Zaregistrujte podrobnosti postdatovaného šeku, který vydáte dodavateli. Při zaúčtování platby odpovědnost dodavatele je rozpoznána, ale na bankovní účet není ještě Dal. Místo toho se pro tento účel používá clearingový účet.</td>
</tr>
<tr class="odd">
<td>Registrace a zaúčtování postdatovaného šeku pro odběratele</td>
<td>Zaregistruje podrobnosti postdatovaného šeku přijatého od odběratele. Při zaúčtování platby pohledávek zákazníka je Dal, ale na bankovní účet není ještě MD. Místo toho se pro tento účel používá clearingový účet.</td>
</tr>
<tr class="even">
<td>Registrovat a zaúčtovat náhradní postdatovaný šek pro zákazníka nebo dodavatele</td>
<td>
V případě ztráty nebo poškození původního šeku pro dodavatele nebo od odběratele můžete vydat náhradní postdatovaný šek. Při registraci detailů šeku zadejte odkaz na původní šek a označte, že nový šek je náhrada za původní. Náhradní šek můžete také zaúčtovat.</td>
</tr>
<tr class="odd">
<td>Přenos postdatovaného šeku odběratele na dodavatele</td>
<td>Když od odběratele obdržíte postdatovaný šek, můžete přenést tento šek na dodavatele jako platbu.</td>
</tr>
<tr class="even">
<td>Vyrovnání postdatovaných šeků pro odběratele nebo dodavatele</td>
<td>Vyrovnejte postdatovaný šek, který je zaúčtován na překlenovací účet odběratele nebo dodavatele, když je šek již splatný. Při vyrovnání šeku je banka již Má dáti nebo Dal s ohledem na clearingový účet, který byl použit dříve.</td>
</tr>
<tr class="odd">
<td>Zrušení postdatovaného šeku pro dodavatele</td>
<td>Zaúčtovaný postdatovaný šek v těchto situacích můžete zrušit:-kontrola je vrácen bankou.
-Kontrola je nesprávná faktura vyrovnána.
-Hotovostní platby provádí proti šeku.
</td>
</tr>
<tr class="even">
<td>Zastavit platbu postdatovaného šeku</td>
<td>Můžete zastavit platbu na postdatovaném šeku vystaveném dodavateli z důvodů, jako je nedostatek finančních prostředků, změna podmínek smlouvy s dodavatelem, vadné zboží u dodavatele, dodání nebo vrácení zboží dodavateli. Můžete zastavit platbu pouze na kontroly, které nebyly vymazány.</td>
</tr>
</tbody>
</table>







