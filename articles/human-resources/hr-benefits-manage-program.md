---
title: Definování a správa programu zaměstnaneckých výhod
description: Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Toto téma obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 54500cad7fe2b48aa4e3b2057f4edcfcf244959e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694928"
---
# <a name="define-and-manage-a-benefits-program"></a>Definování a správa programu zaměstnaneckých výhod


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Human Resources poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Toto téma obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod.

## <a name="benefit-setup"></a>Nastavení výhod

Než bude možné pracovníky přihlásit k zaměstnaneckým výhodám, je nutné vytvořit prvky jednotlivých výhod. Tyto prvky kombinují podobné plány zaměstnaneckých výhod a definují výchozí nastavení, jako jsou například sazby srážek a podrobnosti účetnictví. Mnoho z těchto nastavení lze upravit při pozdějším přihlášení pracovníků k zaměstnanecké výhodě. Pro každý plán zaměstnanecké výhody může organizace nabízet několik možností přihlášení a pracovník se také může zříct přihlášení k plánu. 

[![Tok procesu výhod.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Prvky zaměstnanecké výhody

Před zahájením tvorby zaměstnaneckých výhod a přihlašování pracovníků k nim je nutné definovat prvky, které tvoří zaměstnaneckou výhodu: typ, plán a možnosti.

-   **Typ** – kolekce plánů pro určité zaměstnanecké výhody, jako jsou lékař nebo parkování.
-   **Plán** – zvláštní zaměstnanecké výhody sjednané od zprostředkovatele.
-   **Možnost** – úroveň krytí, například pouze zaměstnanec nebo zaměstnanec a manžel/ka či partner/ka.

Organizace může svým pracovníkům pro každý typ zaměstnanecké výhody (například očního či zubního vyšetření) nabídnout jeden nebo více plánů. Pro každý plán může organizace nabídnout různé možnosti. Například si mohou zaměstnanci zakoupit další období krytí pojištění na úrovni jedno-, dvoj- nebo trojnásobku jejich roční mzdy. Každá kombinace plánu a možností se stane zaměstnaneckou výhodou, ke které se mohou pracovníci přihlásit. 

[![obrázek výhod.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Způsobilost
Mnoho okolností určuje nárok pracovníka na různé typy zaměstnaneckých výhod, které nabízí zaměstnavatel. Když v aplikaci Dynamics 365 Human Resources vytvoříte zaměstnaneckou výhodu, můžete nastavit typ nároku, který se k ní vztahuje. 

Výhodu můžete zpřístupnit pro všechny zaměstnance. Například některé společnosti nabízejí parkovací místa pro všechny zaměstnance jako zaměstnaneckou výhodu. Při vytváření zaměstnanecké výhody nastavíte nárok na možnost **Všichni pracovníci mají nárok**. 

Pro jiné výhody jako obstavení a daňové odvody nárok neplatí. Při vytváření těchto typů výhod nastavujete nárok na **Přeskočit proces nároku**. 

Nárok na zaměstnaneckou výhodu nakonec může být založené na pravidlech. Například společnost nabízí dva druhy pojištění zaměstnancům. Vedení společnosti má nárok na jeden plán životního pojištění, zatímco ostatní zaměstnanci na plný úvazek mají nárok na jiný plán životního pojištění. V aplikaci Human Resources můžete vytvořit pravidlo způsobilosti k uplatnění výhod, pomocí kterého můžete vyhledat všechny zaměstnance ve vedoucích pozicích, a jiné pravidlo k vyhledání všech ostatních zaměstnanců na plný úvazek a pak tato pravidla použít u příslušné výhody.

## <a name="enrollment"></a>Přihlášení
Po vytvoření zaměstnaneckých výhod, které vaše organizace nabízí, a určení nároku můžete k zaměstnaneckým výhodám přihlásit pracovníky. V rámci jednoho procesu můžete k zaměstnaneckým výhodám přihlašovat jednotlivé pracovníky nebo mnoho pracovníků najednou. 

Někdy může organizace přestat nabízet určité zaměstnanecké výhody. V tomto případě je nutné aktualizovat výhodu a pracovníky, kteří jsou v programu zaregistrováni. Hromadné vypršení zaměstnaneckých výhod umožňuje hromadně změnit datum vypršení platnosti zaměstnaneckých výhod a registrace pracovníků registrovaných k dané výhodě. Můžete také vybrat několik pracovníků, kteří jsou registrováni k zaměstnaneckým výhodám, a změnit koncové datum jejich pokrytí. 

Nápodobně vám prodloužení platnosti hromadné registrace zaměstnanecké výhody umožní odložit datum vypršení platnosti zaměstnanecké výhody i registrací pracovníků k dané výhodě, když se rozhodnete zaměstnaneckou výhodu nabízet déle, než jste původně plánovali.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
