---
title: Verze Preview Dynamics 365 Commerce 10.0.30 (listopad 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce 10.0.30.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405550"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Verze Preview Dynamics 365 Commerce 10.0.30 (listopad 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce verze Preview 10.0.30. Tato verze má číslo sestavení 10.0.1362 a je k dispozici podle následujícího plánu:

- **Verze Preview:** září 2022
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2022
- **Obecně dostupné vydání (automatická aktualizace):** Listopad 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---------|------------------|----------------|--------------| 
| Zákaznická podpora   | Chatujte na webu elektronického obchodu pomocí robota Power Virtual Agents. | Tato funkce dá uživatelům webu elektronického obchodování možnost použít chatovacího robota Power Virtual Agents pro žádosti o podporu. | Aktivuje správce/tvůrci pro koncové uživatele |
| Přehledy  |  Streamujte události s provozními informacemi o místě prodeje (POS) do svého účtu Application Insights. | [Přístup k protokolům v Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  Přihlášení IT profesionála/vývojáře   |
|  Platby  | Podpora objednávek PayPal po 29denní autorizační lhůtu. | Maximální doba autorizace pro PayPal je 29 dní, poté musí být vygenerována nová autorizace a ID objednávky. Jako alternativu nabízí PayPal možnost, kdy lze objednávku na objednávku PayPal označit jako obecnou objednávku, což umožňuje více autorizací a zachycení na základě stejného ID objednávky, namísto generování nové autorizace a ID objednávky po 29 dnech). | Při konfiguraci platebního konektoru PayPal v Commerce headquarters bylo přidáno pole **OrderIntent**, které může mít dvě hodnoty:<p><p>- **Autorizovat** - Tato konfigurace je výchozí (pokud pole zůstane prázdné, **Autorizovat** bude fungovat jako výchozí). Konfigurace **OrderIntent** na **Povolit** koreluje s hodnotou PayPal **processing_instruction** **NO_INSTRUCTION**. Objednávka bude autorizována službou PayPal a při použití této hodnoty nelze autorizaci změnit.<p>- **Uložit** – Když je hodnota **OrderIntent** nastavena na **Uložit**, koreluje to s hodnotou PayPal **processing_instruction** **ORDER_SAVED_EXPLICITLY**. Při použití této hodnoty budou odkazy na objednávky uloženy ve službě PayPal.  |
| Přihlášení POS  | [Aktivace funkcí samoobslužné diagnostiky pro přihlášení do POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Tato funkce poskytuje samoobslužné diagnostické funkce v místě prodeje (POS) a Commerce headquarters, aby pomohla zaměstnancům a manažerům prodejen rychle identifikovat a opravit hlavní příčiny problémů s přihlášením do POS.<p><p>- Zprávy o selhání zobrazované na přihlašovací obrazovce POS byly vylepšeny tak, aby poskytovaly konkrétní informace o hlavní příčině, které mohou pomoci zaměstnancům prodejen, kteří používají POS, pochopit, co se pokazilo, aby mohli provést nezbytná opatření k vyřešení problému.<p>- Funkce **Test přihlášení** je k dispozici na stránce **Pracovníci** v Commerce headquarters, aby manažeři prodejen, kteří nastavují POS zařízení, mohli simulovat přihlašování do POS. V případě selhání přihlášení poskytuje tato funkce praktické průvodce odstraňováním problémů, takže manažeři mohou zkontrolovat příslušné konfigurace, opravit problémy a ověřit opravy.  | Zapnuto ve výchozím nastavení |


## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Dynamics 365 Finance 10.0.30 obsahuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.30 finančních a provozních aplikací](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.30, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022](/dynamics365-release-plan/2022wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-features"></a>Odstraněné a zastaralé funkce

Článek [Odstraněné nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) popisuje funkce, které byly pro Commerce odstraněny nebo jsou zastaralé.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
