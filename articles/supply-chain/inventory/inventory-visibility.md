---
title: Přehled doplňku Viditelnost zásob
description: Toto téma vysvětluje, co je Viditelnost zásob a popisuje funkce doplňku.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 644eb0d682c35bd604c188aa02e4a6c69b3ff209
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474981"
---
# <a name="inventory-visibility-add-in-overview"></a>Přehled doplňku Viditelnost zásob

[!include [banner](../includes/banner.md)]

Doplněk Viditelnost zásob (označovaný také jako *Viditelnost zásob*) je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase. Poskytuje tedy globální pohled na zásoby.

Externí systémy přistupují ke službě prostřednictvím RESTful rozhraní API. Tímto způsobem se mohou buď přímo dotazovat na informace o daných sadách dimenzí, nebo provádět změny ve vašem inventáři v různých přizpůsobených zdrojích dat.

Jako mikroslužba, jejímž základem je služba Microsoft Dataverse poskytuje Viditelnost zásob určitou rozšiřitelnost. K vytváření aplikací můžete použít Power Apps. Power BI můžete také použít k poskytování přizpůsobených funkcí, které splňují vaše obchodní požadavky.

Viditelnost zásob můžete integrovat s různými systémy třetích stran nastavením možností konfigurace pro standardizované dimenze zásob a nastavením typů transakcí. Viditelnost zásob také podporuje přizpůsobitelnou rozšiřitelnost prostřednictvím konfigurovatelných vypočítaných množství.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Nastavení integrace Viditelnosti zásob s aplikací Dynamics 365 Supply Chain Management

Integrované řešení čerpá skladová data z Dynamics 365 Supply Chain Management a průběžně sleduje změny zásob. Další informace viz [Instalace a nastavení viditelnosti zásob](inventory-visibility-setup.md) a [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Jak získat globální přehled o zásobách

Integrované řešení vám umožňuje definovat vlastní zdroje dat a centralizovat data zásob. Další informace viz [Konfigurace viditelnosti zásob](inventory-visibility-configuration.md).

Existují dva přístupy k prohlížení vašich zásob:

- Odešlete dotaz prostřednictvím vysoce výkonného rozhraní API. Toto rozhraní API může vracet data o zásobách téměř v reálném čase přímo z instance uložené v mezipaměti. Smlouvy a vzorky najdete v části [Veřejná rozhraní API Viditelnosti zásob](inventory-visibility-api.md).
- Zobrazte nezpracovaný seznam zásob na skladě. Tento seznam je pravidelně synchronizován z instance uložené v mezipaměti a je viditelný v Dataverse. Další informace viz [Aplikace Viditelnost zásob](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Předběžné rezervace

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Předběžná rezervace se použije v případě, kdy si podnik musí rezervovat konkrétní množství produktů, aby podpořil například plnění prodejní objednávky, které zamezí nadměrnému prodeji. Když je prodejní objednávka vytvořena a potvrzena v Supply Chain Management nebo jiných systémech pro správu objednávek, je požadavek na rezervaci množství odeslán do Viditelnosti zásob. Viditelnost zásob vám umožňuje rezervovat produkty s podrobnostmi o dimenzi a konkrétními typy transakcí zásob. (Další informace viz [Aplikace Viditelnost zásob](inventory-visibility-power-platform.md) .) Poté, co je množství úspěšně rezervováno, je vráceno ID rezervace. Toto ID rezervace můžete použít ke zpětnému propojení na původní objednávku v Supply Chain Management nebo v jiných systémech správy objednávek.

Funkce je navržena tak, aby rezervace v doplňku Viditelnost zásob nezměnila celkové množství. Místo toho pouze označí vyhrazené množství. (Z tohoto důvodu se pro ni používá označení *předběžná rezervace*.) Množství s předběžnou rezervací lze kompenzovat, když jsou produkty spotřebovány v Supply Chain Management nebo v systému třetí strany, opětovným zavoláním API k provedení odpočtu množství a aktualizaci celkového množství ve Viditelnosti zásob. Další informace viz [Rezervace ve Viditelnosti zásob](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
