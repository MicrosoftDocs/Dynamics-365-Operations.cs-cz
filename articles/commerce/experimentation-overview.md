---
title: Experimentování v Dynamics 365 Commerce
description: Experimentování umožňuje vytváření, úpravy a správu rozložení stránky a úpravy obsahu v konfigurátoru webů. U stránek a entit elektronického obchodování na stránce je povolena úplná podpora experimentování.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8b2e97167d12b8ceecf72af075ee0362101c4fa0
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930159"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Experimentování v Dynamics 365 Commerce
Pomocí experimentování v Dynamics 365 Commerce můžete ověřovat hypotézy o efektivnosti vašich stránek elektronického obchodování a rozhodovat se na základě dat. Commerce podporuje testování A/B na stránkách, v modulech a fragmentech a umožňuje vám měřit dopad navrhovaných změn na váš web.

V konfigurátoru webů můžete vytvářet, upravovat a spravovat zpracování stránky a obsahu označované jako **varianty** . Commerce integruje služby třetích stran, které můžete používat k vytváření experimentů a přiřazování jednotlivých zpracování. Streamy událostí v reálném čase zaznamenávané v Commerce umožňují provádět analýzu, která definuje výsledky experimentu ve službě třetí strany. Tuto analýzu pak můžete využít k podpoře nebo vyvrácení vaší hypotézy.

## <a name="set-up-prerequisites"></a> Nastavení předpokladů
1. **Získejte správnou verzi Commerce** – Upgradujte knihovnu modulů, sadu SDK pro rozšiřitelnost online kanálů a Commerce Scale Unit na verzi Commerce 10.0.13 nebo novější.
1. **Nastavte konektor pro experimentování** – Konektor pro experimentování umožňuje propojit Commerce se službami třetích stran, aby bylo možné načítat seznam experimentů a určovat, kdy se má experiment zobrazit uživateli. Konektor třetí strany si můžete zakoupit na webu [AppSource](https://appsource.microsoft.com). Postupujte podle pokynů k nastavení poskytnutých vydavatelem. Jako alternativu můžete použít ukázkový testovací konektor z Commerce a otestovat pracovní postup experimentování, aniž byste museli konfigurovat externí službu. Další informace najdete v tématu [Konfigurace a povolení konektorů](e-commerce-extensibility/connectors.md). 
1. **Zapněte v Commerce příznaky funkce experimentování** – Experimentování můžete povolit na úrovni tenanta tak, že přejdete na **Nastavení tenanta > Funkce** , nebo na úrovni webu v **Nastavení webu > Funkce** .
    - Když povolíte příznak **Experimentování** , můžete v experimentech vytvářet varianty modulů na stránce bez ovlivnění nebo kopírování dalšího obsahu, který není součástí experimentu. Tím je zajištěno, že průběžné aktualizace obsahu mimo experiment zůstanou synchronizované během celého životního cyklu experimentu. Když tento příznak zakážete, zastaví se zobrazování všech experimentů uživatelům a odeberou se všechny funkce pro úpravy v konfigurátoru webů.
    - Když povolíte příznak **Experimentovat na stránkách nebo ve fragmentech** , můžete spouštět experimenty na stránce nebo ve fragmentu. Tím se vytvoří kopie úplné instance celé stránky nebo fragmentu pro všechny moduly v rámci stránky nebo fragmentu. Tento režim použijte, pokud chcete otestovat komplexní změny obsahu nebo v případě, že synchronizace průběžných změn obsahu napříč instancemi není problém. Zakázání tohoto příznaku zabrání vytváření a úpravám nových experimentů na stránkách a ve fragmentech.
    > [!NOTE]
    > Aby funkce **Experimentovat na stránkách nebo ve fragmentech** fungovala, musí být povolen také příznak **Experimentování** .
    
## <a name="experimentation-lifecycle"></a>Životní cyklus experimentování
Nastavení experimentu, vytváření variant a spuštění experimentu je iterativní proces. Na schématu níže je znázorněn životní cyklus experimentování v Commerce a ve službě třetí strany. 

[ ![Životní cyklus experimentování](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Další informace o jednotlivých krocích v procesu experimentování najdete v následujících tématech.
- [Identifikace hypotézy a určení metriky experimentu](experimentation-identify.md)
- [Nastavení experimentu](experimentation-setup.md)
- [Připojení a úpravy experimentu](experimentation-connect-edit.md)
- [Náhled a publikování experimentu](experimentation-preview-publish.md)
- [Spuštění a monitorování experimentu](experimentation-run-monitor.md)
- [Povýšení varianty a dokončení experimentu](experimentation-review-complete.md)

> [!NOTE]
> Pokud se chcete dozvědět, kde v životním cyklu se experiment nachází, přejděte na kartu **Experimenty** v konfigurátoru webů. Zobrazí se seznam experimentů se stavem každého experimentu v Commerce i ve službě třetí strany. Další informace najdete v tématu [Kontrola stavu experimentu](experimentation-status.md).

## <a name="next-step"></a>Další krok
[Identifikace hypotézy a určení metriky úspěšnosti experimentu](experimentation-identify.md) 
