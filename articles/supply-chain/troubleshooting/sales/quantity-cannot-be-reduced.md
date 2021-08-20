---
title: Množství nelze při zrušení prodejní objednávky snížit
description: Množství nelze při zrušení prodejní objednávky snížit.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752627"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Množství nelze při zrušení prodejní objednávky snížit

Kód chyby: SYS138831

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Množství nelze snížit. Počet transakcí zásob u objednávky je příliš nízký, protože na množství nebo její část odkazuje výstupní objednávka nebo výrobní zakázka nebo je označeno vůči jiným transakcím.

## <a name="cause"></a>Příčina

Pokud je práce přidružená k prodejní objednávce, nemůžete zrušit prodejní objednávku, dokud nebude práce zrušena a stornována. Tento požadavek platí, i když je práce přidružená k prodejní objednávce uzavřena.

## <a name="resolution"></a>Řešení

Chcete-li problém opravit, proveďte následující úkoly:

1. Zrušte otevřenou práci.
1. Odstraňte vytížení.
1. Snižte vyskladněné množství.

### <a name="cancel-open-work"></a>Zrušení otevřené práce

Chcete-li zrušit otevřenou práci, postupujte takto.

1. Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.
1. V poli **ID práce** zadejte ID práce, kterou chcete zrušit a které aktuálně obsahuje pro možnost **Stav práce** hodnotu *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinované* nebo *Uzavřené*.
1. Vyberte **OK**.
1. Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.

### <a name="delete-the-load"></a>Odstranění vytížení

Chcete-li odstranit vytížení, postupujte takto:

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Otevřete příslušnou prodejní objednávku.
1. Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti práce**.
1. Na stránce **Práce** v podokně Akce na kartě **Práce** ve skupině **Práce** vyberte příkaz **Zrušit práci**.
1. Potvrďte, že se pole **Stav práce** nastaví na *Zrušeno*.
1. Zavřete stránku **Práce**.
1. Na stránce podrobností prodejní objednávky na záložce s náhledem **Řádky prodejní objednávky** vyberte **Sklad \> Načíst podrobnosti**.
1. V podokně Akce zvolte **Odstranit**.
1. Výběrem **Ano** potvrďte, že chcete odstranit vytížení.
1. Zavřete stránku **Vytížení**.

### <a name="reduce-the-picked-quantity"></a>Snížení vyskladněného množství

Po zrušení všech prací snižte vyskladněné množství podle těchto kroků.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Otevřete příslušnou prodejní objednávku.
1. Na záložce s náhledem **Řádky prodejní objednávky** vyberte v panelu nástrojů **Aktualizovat řádek \> Vydat**.
1. Na stránce **Vydat** v části **Transakce** vyberte řádek, kde je pole **Stav výdeje** nastaveno na *Vydáno*.
1. V části **Transakce** vyberte v panelu nástrojů **Přidat řádek výdeje**.
1. V části **Řádky výdeje** vyberte v panelu nástrojů **Potvrdit výběr všech**.
1. Zavřete stránku **Vydat**.
1. Na stránce podrobností prodejní objednávky v podokně akcí na kartě **Prodejní objednávka** ve skupině **Udržovat** vyberte **Zrušit**.
1. Vyberte možnost **Ano** k potvrzení, že chcete prodejní objednávku zrušit.
