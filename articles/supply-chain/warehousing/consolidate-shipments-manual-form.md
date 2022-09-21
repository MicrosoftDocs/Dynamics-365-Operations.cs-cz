---
title: Ruční konsolidace dodávek pomocí stránky konsolidace dodávek
description: Tento článek představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno pomocí stránky konsolidace dodávek.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 05f094b82b3d9bf9c095bc43f404aa7159bcafba
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427897"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Ruční konsolidace dodávek pomocí stránky konsolidace dodávek

[!include [banner](../includes/banner.md)]

Tento článek představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno pomocí stránky **Konsolidace dodávek**.

## <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Scénář v tomto článku odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Nastavení zásad konsolidace dodávek a filtry produktů

Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány. Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.

## <a name="create-the-sales-orders-for-this-scenario"></a>Vytvoření prodejních objednávek pro tento scénář

Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat. Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS). Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.

Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.

### <a name="create-sales-orders-1-and-2"></a>Vytvoření prodejních objednávek 1 a 2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Fond:** *ShipCons*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

### <a name="create-sales-orders-3-and-4"></a>Vytvoření prodejních objednávek 3 a 4

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Fond:** Pole ponechejte prázdné.

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

## <a name="release-the-orders-to-the-warehouse"></a>Uvolnění objednávek do skladu

Chcete-li uvolnit každou prodejní objednávku, kterou jste vytvořili pro tento scénář, do skladu, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.
1. Vyhledejte a vyberte prodejní objednávku, kterou chcete uvolnit.
1. V podokně akcí na kartě **Sklad** vyberte **Akce \> Uvolnit do skladu** pro uvolnění vybrané prodejní objednávky.
1. Tento postup opakujte pro každou další prodejní objednávku, kterou jste vytvořili pro tento scénář.

## <a name="consolidate-shipments"></a>Konsolidovat dodávky

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Najděte a vyberte dodávku, která byla vytvořena při uvolnění prodejní objednávky 1 do skladu. (Její pole **Zásada konsolidace dodávky** by mělo být nastaveno na *Fond objednávek* .)
1. V podokně akcí na kartě **Dodávky** zvolte **Dodávky \> Konsolidovat dodávky**.
1. Ověřte dodávky, které jsou navrženy pro konsolidaci. Ke konsolidaci by měla být navržena pouze jedna dodávka, která má stejnou zásadu.
1. Zavřete stránku **Konsolidace dodávek**.
1. Najděte a vyberte dodávku, která byla vytvořena při uvolnění prodejní objednávky 3 do skladu. (Její pole **Zásada konsolidace dodávky** by mělo být nastaveno na *Výchozí* .)
1. V podokně akcí na kartě **Dodávky** zvolte **Dodávky \> Konsolidovat dodávky**.
1. Ověřte, že nejsou navrženy žádné dodávky pro konsolidaci.
1. Vyberte **Zobrazit filtry**.
1. V podokně **Filtry** odeberte filtr **Číslo objednávky** a poté vyberte **Použít**.
1. Ověřte dodávky, které jsou navrženy pro konsolidaci. Ke konsolidaci by měla být navržena pouze jedna dodávka, která má stejnou zásadu.

## <a name="additional-resources"></a>Další prostředky

- [Přehled zásad konsolidace dodávek](about-shipment-consolidation-policies.md)
- [Konfigurace zásad konsolidace dodávek](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]