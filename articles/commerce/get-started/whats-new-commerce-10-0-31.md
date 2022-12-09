---
title: Verze Preview aplikace Dynamics 365 Commerce 10.0.31 (únor 2023)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787519"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Verze Preview aplikace Dynamics 365 Commerce 10.0.31 (únor 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce verze Preview 10.0.31. Tato verze má číslo sestavení 10.0.1406 a je k dispozici podle následujícího plánu:

- **Verze Preview:** Říjen 2022
- **Obecně dostupné vydání (automatická aktualizace):** Leden 2023
- **Obecně dostupné vydání (automatická aktualizace):** Únor 2023

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a |
|---|---|---|---|
| Kódy chyb | Commerce nově obsahuje standardizované odkazy na chyby, které mají být zahrnuty do chyb při placení online kanálů prezentovaných online nakupujícím.| [Kódy chyb modulu pokladny](../checkout-module-error-codes.md)  | Zapnuto ve výchozím nastavení |
| Platby | [Aktivace Apple Pay u Dynamics 365 Connector pro Adyen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | Zákazníci elektronického obchodu mohou používat Apple Pay na stránkách košíku a pokladny, když používají podporovaná zařízení nebo prohlížeče. | Přihlášení vývojáře |
| Platby  |  Commerce nově obsahuje možnost omezit interakci uživatelů s opakujícími se platebními tokeny v uživatelském rozhraní Commerce headquarters. Platební formuláře, jako např. stránka **Prodejní objednávka call centra**, již nebude zobrazovat dříve používaný token opakované platby zákazníka pro použití v nové transakci. Pouze určené zadání „karta v evidenci“ vstup na obrazovku **Zákaznické platby** Commerce nebo po dohodě se zákazníkem při platbě prostřednictvím prodejní objednávky se zobrazí uživatelům call centra nebo Commerce headquarters při zpracování platby za novou transakci. | [Omezení používání platebních tokenů](../dev-itpro/limit-token-usage.md)  |  Správa funkcí<p>*Omezení použití platebního tokenu na kontext objednávky*  |
| POS | [Vytvoření nákupních objednávek z POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Vylepšená operace příchozích skladových zásob v aplikaci pokladního místa (POS) umožňuje uživatelům vytvářet, upravovat a potvrzovat požadavky na nákupní objednávky. |  Správa funkcí<p>*Možnost vytvořit požadavek na nákupní objednávku v POS*   |
| K dispozici jsou další jazyky | K dispozici jsou další čtyři jazyky | V seznamu preferovaných jazyků jsou pro uživatele k dispozici čtyři nové jazyky: korejština, portugalština (Portugalsko), vietnamština a čínština (tradiční). Chcete-li vybrat tuto možnost, přejděte na **Uživatelské možnosti \> Předvolby \> Předvolby jazyka a země/oblasti**. | Lokalizované předvolby |  



## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Commerce 10.0.31 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.31 finančních a provozních aplikací (únor 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.31, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si článek [znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022](/dynamics365-release-plan/2022wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-commerce-features"></a>Odstraněné a zastaralé funkce Commerce

Článek [Odstraněné nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) popisuje funkce, které byly pro Commerce odstraněny nebo jsou zastaralé.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 měsíců před odebráním.


U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
