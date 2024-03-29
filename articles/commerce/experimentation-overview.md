---
title: Experimentování v Dynamics 365 Commerce
description: Experimentování umožňuje vytváření, úpravy a správu rozložení stránky a úpravy obsahu v konfigurátoru webů. U stránek a entit elektronického obchodování na stránce je povolena úplná podpora experimentování.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946196"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Experimentování v Dynamics 365 Commerce
Pomocí experimentování v Dynamics 365 Commerce můžete ověřovat hypotézy o efektivnosti vašich stránek elektronického obchodování a rozhodovat se na základě dat. Commerce podporuje testování A/B na stránkách, v modulech a fragmentech a umožňuje vám měřit dopad navrhovaných změn na váš web.

V konfigurátoru webů Commerce můžete vytvářet, upravovat a spravovat zpracování stránky a obsahu označované jako **varianty**. Commerce integruje služby třetích stran, které můžete používat k vytváření experimentů a přiřazování jednotlivých zpracování. Streamy událostí v reálném čase zaznamenávané v Commerce umožňují provádět analýzu, která definuje výsledky experimentu ve službě třetí strany. Tuto analýzu pak můžete využít k podpoře nebo vyvrácení vaší hypotézy.

## <a name="set-up-prerequisites"></a> Nastavení předpokladů

1. **Získejte správnou verzi Commerce** – Upgradujte knihovnu modulů, sadu software development kit (SDK) pro rozšiřitelnost online kanálů a Commerce Scale Unit na verzi Commerce 10.0.13 nebo novější.
1. **Nastavte konektor pro experimentování** – Konektor pro experimentování umožňuje propojit Commerce se službami třetích stran, aby bylo možné načítat seznam experimentů a určovat, kdy se má experiment zobrazit uživateli. Konektor třetí strany si můžete zakoupit na webu [AppSource](https://appsource.microsoft.com). Postupujte podle pokynů k nastavení poskytnutých vydavatelem. Jako alternativu můžete použít ukázkový testovací konektor z Commerce a otestovat pracovní postup experimentování, aniž byste museli konfigurovat externí službu. Další informace najdete v tématu [Konfigurace a povolení konektorů](e-commerce-extensibility/connectors.md). 
1. **Zapněte v Commerce příznaky funkce experimentování** – Experimentování můžete povolit na úrovni tenanta tak, že přejdete na **Nastavení tenanta \> Funkce**, nebo na úrovni webu v **Nastavení webu \> Funkce**. Zapněte příznak **Experimentování** pro zahájení vytváření variant modulů. Když tento příznak zakážete, zastaví se zobrazování všech experimentů uživatelům a odeberou se všechny funkce pro úpravy v konfigurátoru webů.
    
## <a name="experimentation-lifecycle"></a>Životní cyklus experimentování

Nastavení experimentu, vytváření variant a spuštění experimentu je iterativní proces. Na schématu níže je znázorněn životní cyklus experimentování v Commerce a ve službě třetí strany. 

[ ![Životní cyklus experimentování.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Další informace o jednotlivých krocích v procesu experimentování najdete v následujících článcích.
- [Identifikace hypotézy a určení metriky experimentu](experimentation-identify.md)
- [Nastavení experimentu](experimentation-setup.md)
- [Připojení a úprava experimentu](experimentation-connect-edit.md)
- [Náhled a publikování experimentu](experimentation-preview-publish.md)
- [Spuštění a monitorování experimentu](experimentation-run-monitor.md)
- [Propagace varianty a dokončení experimentu](experimentation-review-complete.md)

> [!NOTE]
> Pokud se chcete dozvědět, kde v životním cyklu se experiment nachází, vyberte **Experimenty** v levém navigačním okně konfigurátoru webů. Zobrazí se seznam experimentů se stavem každého experimentu v Commerce i ve službě třetí strany. Další informace najdete v tématu [Kontrola stavu experimentu](experimentation-status.md).

## <a name="next-step"></a>Další krok
[Identifikace hypotézy a určení metriky úspěšnosti experimentu](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
