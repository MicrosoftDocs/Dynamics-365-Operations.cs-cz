---
title: Odhlášení z kolekce událostí webové aktivity
description: Toto téma vysvětluje, jak můžete dovolit návštěvníkům vašeho webu odhlásit se ze sbírání událostí webové aktivity v Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791550"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Odhlášení z kolekce událostí webové aktivity
[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak můžete zákazníkům dovolit odhlásit se ze sbírání událostí webové aktivity v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce dovoluje správcům webu analyzovat webovou aktivitu uživatelů svých e-commerce webů. Tímto způsobem mohou lépe porozumět tomu, jak jsou jejich stránky používány, a mohou je optimalizovat tak, aby poskytovaly lepší uživatelský dojem a splňovaly obchodní cíle.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Způsoby, jak správci mohou uplatnit možnost odhlášení

Správci mají tři možnosti, jak uplatnit možnost odhlášení.

### <a name="opt-out-on-behalf-of-users"></a>Odhlášení jménem uživatelů

V modulu Správa účtu v centrále obchodu se správci mohou odhlašovat jménem uživatelů.

1. V klientovi centrály obchodu na stránce **Všichni zákazníci** vyhledejte a vyberte zákazníka.
1. Na stránce s podrobnostmi zákazníka, na pevné záložce **Maloobchod**, v sekci **Soukromí**, nastavte možnost **Nesledujte aktivitu na webu** na **Ano**.

    ![Nastavení ochrany osobních údajů](media/Disablepersonalizationpart2.png)

1. Zvolte **Uložit** a pak zavřete stránku.

### <a name="module-based-opt-out-experience"></a>Použití funkce odhlášení na základě modulu

Správci mohou nechat ověřené uživatele, aby se sami odhlásili ze sběru událostí webové aktivity. Chcete-li tyto možnosti odhlášení poskytnout, přidejte do stránek profilu účtu odběratele modul odhlášení uživatele.

### <a name="custom-extensions"></a>Vlastní rozšíření

Správci mohou vytvářet svá vlastní rozšíření pro správu možnosti odhlášení pro uživatele. Další informace naleznete v tématu [Volání rozhraní API serveru](e-commerce-extensibility/call-retail-server-apis.md) a [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
