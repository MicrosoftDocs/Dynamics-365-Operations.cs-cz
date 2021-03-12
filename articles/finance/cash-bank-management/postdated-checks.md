---
title: Postdatované šeky
description: Tento článek obsahuje informace o podpoře pro postdatované šeky v aplikaci Microsoft Dynamics 365 Finance. Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu. Takže lze šek proplatit až od určeného data.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f30b8d1061eb2fe709df38628acd798448c8929e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989220"
---
# <a name="postdated-checks"></a>Postdatované šeky

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o podpoře pro postdatované šeky. Postdatované šeky jsou šeky, které jsou vydány za účelem provedení a přijetí platby v budoucí datu. Takže lze šek proplatit až od určeného data.

Dynamics 365 Finance podporuje úplné řízení cyklu postdatovaných šeků v pohledávkách i závazcích, jak znázorňuje následující tabulka.
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
<td>Zaregistrujte podrobnosti postdatovaného šeku, který vydáte dodavateli. Při zaúčtování platby je uznán pasiv dodavatele, avšak bankovní účet není dosud Dal. Místo toho se pro tento účel používá clearingový účet. </td>
</tr>
<tr class="odd">
<td>Registrace a zaúčtování postdatovaného šeku pro odběratele</td>
<td>Zaregistruje podrobnosti postdatovaného šeku přijatého od odběratele. Při zaúčtování platby je pohledávka odběratele Dal, avšak bankovní účet není ještě Má dáti. Místo toho se pro tento účel používá clearingový účet.</td>
</tr>
<tr class="even">
<td>Zaregistruje a zaúčtujte náhradní postdatovaný šek pro odběratele nebo dodavatele.</td>
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
<td>Zaúčtovaný postdatovaný šek v těchto situacích můžete zrušit: - šek je vrácen bankou.
- Šek je použit k nesprávné faktuře.
- Proti šeku je provedena hotovostní platba.
  </td>
  </tr>
  <tr class="even">
  <td>Zastavte platbu postdatovaného šeku.</td>
  <td>Můžete zastavit platbu na postdatovaném šeku vystaveném dodavateli z důvodů, jako je nedostatek finančních prostředků, změna podmínek smlouvy s dodavatelem, vadné zboží u dodavatele, dodání nebo vrácení zboží dodavateli. Můžete zastavit platbu pouze u šeků, které nebyly proplaceny.</td>
  </tr>
  </tbody>
  </table>



Další informace naleznete v následujících tématech:

[Nastavení postdatovaných šeků](tasks/set-up-postdated-checks.md)

[Registrace a zaúčtování postdatovaného šeku pro odběratele](tasks/register-post-postdated-check-customer.md)

[Vyrovnání postdatovaného šeku od odběratele](tasks/settle-postdated-check-customer.md)

[Registrace a zaúčtování postdatovaného šeku pro dodavatele](tasks/register-post-postdated-check-vendor.md) 

[Vyrovnání postdatovaného šeku pro dodavatele](tasks/settle-postdated-check-vendor.md)



