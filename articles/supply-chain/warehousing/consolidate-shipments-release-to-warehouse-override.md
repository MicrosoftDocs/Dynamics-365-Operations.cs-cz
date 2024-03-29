---
title: Konsolidujte zásilky, když dojde k přepsání zásad konsolidace zásilek
description: Tento článek představuje scénář, ve kterém musí být jeden nebo více řádků prodeje ručně uvolněn do skladu ze stránky uvolnění do skladu a před uvolněním musí být přepsána zásada konsolidace dodávek definovaná systémem.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427948"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Konsolidujte zásilky, když dojde k přepsání zásad konsolidace zásilek

[!include [banner](../includes/banner.md)]

Tento článek představuje scénář, ve kterém musí být jeden nebo více řádků prodeje ručně uvolněn do skladu ze stránky **uvolnění do skladu** a před uvolněním musí být přepsána zásada konsolidace dodávek definovaná systémem. Může být vyžadováno přepsání zásady konsolidace dodávek, pokud například objednávka, která není obvykle konsolidována s otevřenými dodávkami, musí být konsolidována s otevřenými dodávkami.

Během scénáře vytvoříte sadu prodejních objednávek a poté před uvolněním objednávek do skladu přepíšete výchozí zásadu konsolidace dodávek.

## <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Scénář v tomto článku odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Nastavení zásad konsolidace dodávek a filtry produktů

Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány. Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.

## <a name="create-the-sales-orders-for-this-scenario"></a>Vytvoření prodejních objednávek pro tento scénář

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte tři identické prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-002*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Uvolněte prodejní objednávky ze stránky Uvolnění do skladu

Postupujte podle těchto kroků a přepište zásadu konsolidace dodávek během uvolnění do skladu.

1. Přejděte na **Řízení skladu \> Uvolnění do skladu \> Uvolnění do skladu**.
1. V horním podokně vyberte první prodejní objednávku, kterou jste vytvořili pro tento scénář.
1. Vyberte **Přidat** a přidejte řádek do vydání do skladu. Všimněte si, že *Výchozí* zásada konsolidace dodávek je použita ve spodním podokně.
1. Ve spodním podokně zvolte **Vybrat zásady konsolidace dodávky**.
1. Vyberte zásadu, která umožňuje konsolidaci s ostatními otevřenými dodávkami stejné zásady. Například vyberte zásadu *CustomerOrderNo*.
1. Vyberte **Uvolnění do skladu**.
1. Vyberte druhou a třetí prodejní objednávku, které jste vytvořili pro tento scénář.
1. Vyberte **Přidat** a přidejte řádky do vydání do skladu. Všimněte si, že *Výchozí* zásada je použita ve spodním podokně.
1. Vyberte druhý řádek a poté v poli **Vybrat novou zásadu konsolidace dodávek** vyberte zásadu *CustomerOrderNo*.
1. Vyberte **Uvolnění do skladu** pro obě řádky.

## <a name="verify-the-shipments"></a>Ověření dodávek

Měly být vytvořeny dvě dodávky:

- První dodávka obsahuje dva řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.
- Druhá dodávka obsahuje jeden řádek a byla vytvořena pomocí zásady konsolidace dodávek *Výchozí*.

Použijte tyto kroky ke kontrole vytvořených dodávek.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Najděte a vyberte požadovanou dodávku.
1. V poli **Zásady konsolidace dodávek** zkontrolujte zásadu konsolidace použitou při vytvoření dodávky.

## <a name="additional-resources"></a>Další prostředky

- [Přehled zásad konsolidace dodávek](about-shipment-consolidation-policies.md)
- [Konfigurace zásad konsolidace dodávek](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]