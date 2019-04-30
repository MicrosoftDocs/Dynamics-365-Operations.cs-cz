---
title: Definování a správa programu zaměstnaneckých výhod
description: Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Tento článek obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 033377f7d45bfa2b798c098be2dde0c21739bb51
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "857423"
---
# <a name="define-and-manage-a-benefits-program"></a>Definování a správa programu zaměstnaneckých výhod

[!include [banner](includes/banner.md)]

Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Toto téma obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod.

<a name="benefit-setup"></a>Nastavení výhod
-------------

Než bude možné pracovníky přihlásit k zaměstnaneckým výhodám, je nutné vytvořit prvky jednotlivých výhod. Tyto prvky kombinují podobné plány zaměstnaneckých výhod a definují výchozí nastavení, jako jsou například sazby srážek a podrobnosti účetnictví. Mnoho z těchto nastavení lze upravit při pozdějším přihlášení pracovníků k zaměstnanecké výhodě. Pro každý plán zaměstnanecké výhody může organizace nabízet několik možností přihlášení a pracovník se také může zříct přihlášení k plánu. 

[![Tok procesu výhod](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Prvky zaměstnanecké výhody
Před zahájením tvorby zaměstnaneckých výhod a přihlašování pracovníků k nim je nutné definovat prvky, které tvoří zaměstnaneckou výhodu: typ, plán a možnosti.

-   **Typ** – kolekce plánů pro určité zaměstnanecké výhody, jako jsou lékař nebo parkování.
-   **Plán** – zvláštní zaměstnanecké výhody sjednané od zprostředkovatele.
-   **Možnost** – úroveň krytí, například pouze zaměstnanec nebo zaměstnanec a manžel/ka či partner/ka.

Organizace může svým pracovníkům pro každý typ zaměstnanecké výhody (například očního či zubního vyšetření) nabídnout jeden nebo více plánů. Pro každý plán může organizace nabídnout různé možnosti. Například si mohou zaměstnanci zakoupit další období krytí pojištění na úrovni jedno-, dvoj- nebo trojnásobku jejich roční mzdy. Každá kombinace plánu a možností se stane zaměstnaneckou výhodou, ke které se mohou pracovníci přihlásit. 

[![obrázek výhod](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Způsobilost
Mnoho okolností určuje nárok pracovníka na různé typy zaměstnaneckých výhod, které nabízí zaměstnavatel. Když v aplikaci Microsoft Talent vytvoříte zaměstnaneckou výhodu, můžete nastavit typ nároku, který se k ní vztahuje. 

Výhodu můžete zpřístupnit pro všechny zaměstnance. Například některé společnosti nabízejí parkovací místa pro všechny zaměstnance jako zaměstnaneckou výhodu. Při vytváření zaměstnanecké výhody nastavíte nárok na možnost **Všichni pracovníci mají nárok**. 

Pro jiné výhody jako obstavení a daňové odvody nárok neplatí. Při vytváření těchto typů výhod nastavujete nárok na **Přeskočit proces nároku**. 

Nárok na zaměstnaneckou výhodu nakonec může být založené na pravidlech. Například společnost nabízí dva druhy pojištění zaměstnancům. Vedení společnosti má nárok na jeden plán životního pojištění, zatímco ostatní zaměstnanci na plný úvazek mají nárok na jiný plán životního pojištění. V aplikaci Talent můžete vytvořit pravidlo způsobilosti k uplatnění výhod, pomocí kterého můžete vyhledat všechny zaměstnance ve vedoucích pozicích, a jiné pravidlo k vyhledání všech ostatních zaměstnanců na plný úvazek a pak tato pravidla použít u příslušné výhody.

## <a name="enrollment"></a>Přihlášení
Po vytvoření zaměstnaneckých výhod, které vaše organizace nabízí, a určení nároku můžete k zaměstnaneckým výhodám přihlásit pracovníky. V rámci jednoho procesu můžete k zaměstnaneckým výhodám přihlašovat jednotlivé pracovníky nebo mnoho pracovníků najednou. 

Někdy může organizace přestat nabízet určité zaměstnanecké výhody. V tomto případě je nutné aktualizovat výhodu a pracovníky, kteří jsou v programu zaregistrováni. Hromadné vypršení zaměstnaneckých výhod umožňuje hromadně změnit datum vypršení platnosti zaměstnaneckých výhod a registrace pracovníků registrovaných k dané výhodě. Můžete také vybrat několik pracovníků, kteří jsou registrováni k zaměstnaneckým výhodám, a změnit koncové datum jejich pokrytí. 

Nápodobně vám prodloužení platnosti hromadné registrace zaměstnanecké výhody umožní odložit datum vypršení platnosti zaměstnanecké výhody i registrací pracovníků k dané výhodě, když se rozhodnete zaměstnaneckou výhodu nabízet déle, než jste původně plánovali.

<a name="additional-resources"></a>Další zdroje
--------

[Zásady způsobilosti k zaměstnaneckým výhodám](benefit-eligibility-policies.md)



