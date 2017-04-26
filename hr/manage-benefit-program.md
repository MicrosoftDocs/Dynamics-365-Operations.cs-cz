---
title: "Definovat a spravovat výhody programu"
description: "Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Tento článek obsahuje informace o postupu nastavení a správy zaměstnaneckých výhod."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definovat a spravovat výhody programu

[!include[banner](includes/banner.md)]


Lidské zdroje poskytují řadu nástrojů, které vám pomohou k nastavení a správě zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance. Toto téma obsahuje informace o tom, jak nastavit spravovat výhody.

<a name="benefit-setup"></a>Nastavení zaměstnaneckých výhod
-------------

Než bude možné pracovníky přihlásit k zaměstnaneckým výhodám, je nutné vytvořit prvky jednotlivých výhod. Tyto prvky kombinují podobné plány zaměstnaneckých výhod a definují výchozí nastavení, jako jsou například sazby srážek a podrobnosti účetnictví. Mnoho z těchto nastavení lze upravit při pozdějším přihlášení pracovníků k zaměstnanecké výhodě. Pro každý plán zaměstnanecké výhody může organizace nabízet několik možností přihlášení a pracovník se také může zříct přihlášení k plánu. 

[![Tok zpracování dávky](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Prvky zaměstnanecké výhody
Před zahájením tvorby zaměstnaneckých výhod a přihlašování pracovníků k nim je nutné definovat prvky, které tvoří zaměstnaneckou výhodu: typ, plán a možnosti.

-   **Typ** – kolekce plánů pro určité zaměstnanecké výhody, jako jsou lékař nebo parkování.
-   **Plán** – zvláštní zaměstnanecké výhody sjednané od zprostředkovatele.
-   **Možnost** – úroveň krytí, například pouze zaměstnanec nebo zaměstnanec a manžel/ka či partner/ka.

Organizace může svým pracovníkům pro každý typ zaměstnanecké výhody (například očního či zubního vyšetření) nabídnout jeden nebo více plánů. Pro každý plán může organizace nabídnout různé možnosti. Například si mohou zaměstnanci zakoupit další období krytí pojištění na úrovni jedno-, dvoj- nebo trojnásobku jejich roční mzdy. Každá kombinace plánu a možností se stane zaměstnaneckou výhodou, ke které se mohou pracovníci přihlásit. 

[![Výhoda pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Způsobilost
Mnoho okolností určuje nárok pracovníka na různé typy zaměstnaneckých výhod, které nabízí zaměstnavatel. Při vytváření výhodu v 365 Microsoft Dynamics pro operace můžete nastavit typ způsobilosti vztahující se k této zaměstnanecké výhody. 

Výhodu můžete zpřístupnit pro všechny zaměstnance. Například některé společnosti nabízejí parkovací průchody pro všechny zaměstnance jako zaměstnaneckých výhod. Při vytváření zaměstnanecké výhody nastavíte nárok na možnost **Všichni pracovníci mají nárok**. 

Pro jiné dávky jako garnishments a dávky, daně se nevztahuje nárok. Syrovátka vytvořit tyto typy dávek, nastavte nároku na **obejít proces nároku na**. 

Nároku na zaměstnaneckou výhodu nakonec může být založené na pravidlech. Například společnost nabízí dva druhy pojištění výhody zaměstnancům. Výkonné zaměstnance jsou způsobilé pro jeden plán životního pojištění, že jsou způsobilé pro ostatní pojištění plán všech ostatních zaměstnanců na plný úvazek. V 365 Dynamics pro operace můžete vytvořit pravidlo způsobilosti výhody najít všechny výkonné zaměstnance a jiné pravidlo pro vyhledání všech ostatních zaměstnanců na plný úvazek a pak použít pravidla ve prospěch příslušné.

## <a name="enrollment"></a>Přihlášení
Po vytvoření zaměstnaneckých výhod, které vaše organizace nabízí, a určení nároku můžete k zaměstnaneckým výhodám přihlásit pracovníky. V rámci jednoho procesu můžete k zaměstnaneckým výhodám přihlašovat jednotlivé pracovníky nebo mnoho pracovníků najednou. 

Někdy může organizace přestat nabízet určité zaměstnanecké výhody. V tomto případě je nutné aktualizovat výhody a pracovníky, kteří jsou zaregistrováni v. Hmotnost výhody vypršení umožňuje změnit datum vypršení platnosti výhodu a přihlášení pracovníka pro tyto výhody najednou. Můžete také vybrat několik pracovníků, kteří jsou registrováni k zaměstnaneckým výhodám, a změnit koncové datum jejich pokrytí. 

Nápodobně vám prodloužení platnosti hromadné registrace zaměstnanecké výhody umožní odložit datum vypršení platnosti zaměstnanecké výhody i registrací pracovníků k dané výhodě, když se rozhodnete zaměstnaneckou výhodu nabízet déle, než jste původně plánovali.

<a name="see-also"></a>Viz také
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)




