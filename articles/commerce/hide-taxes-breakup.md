---
title: Skrytí informací o daňovém rozdělení v souhrnech objednávek
description: Toto téma popisuje, jak se v aplikaci Microsoft Dynamics 365 Commerce dají skrýt informace o daňovém rozdělení v souhrnech objednávek na stránkách košíku, pokladny, v potvrzení objednávky a podrobnostech objednávky.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645213"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Skrytí informací o daňovém rozdělení v souhrnech objednávek

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje, jak se v aplikaci Microsoft Dynamics 365 Commerce dají skrýt informace o daňovém rozdělení v souhrnech objednávek na stránkách košíku, pokladny, v potvrzení objednávky a podrobnostech objednávky.

Ve výchozím nastavení aplikace Dynamics 365 Commerce zobrazuje informace o daňovém rozdělení v souhrnech objednávek na stránkách košíku, pokladny, v potvrzení objednávky a podrobnostech objednávky. Od verze Commerce 10.0.27 obsahuje konfigurátor webu Commerce možnost, která vám umožní skrýt informace o daňovém rozdělení v souhrnech objednávek.

Na následujícím obrázku je příklad dvou souhrnů objednávky. První zobrazuje informace o daňovém rozdělení, druhý je skrývá.

![Příklady vozíků, kde jsou zobrazeny a skryty informace o daňovém rozdělení.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Možnost skrýt informace o daňovém rozdělení v souhrnech objednávek je dostupná pouze v případě, kdy je možnost **Ceny zahrnují DPH** pro kanál elektronického obchodování nastavena v centrále Commerce na **Ano** v nabídce **Maloobchod a obchod \> Kanály \> Obchody \> Všechny obchody**. 
> - Ve výchozím nastavení je možnost **Zobrazit rozdělení daní v souhrnu objednávky** v konfigurátoru webu povolena.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Skrytí informací o daňovém rozdělení v souhrnech objednávek

Chcete-li skrýt informace o daňovém rozdělení v souhrnech objednávek, postupujte takto.

1. V konfigurátoru webů Commerce přejděte na web, který chcete aktualizovat.
1. Přejděte na **Nastavení webu \> Rozšíření**.
1. Vypněte zaškrtávací políčko **Zobrazit rozdělení daní v souhrnu objednávky**.

Chcete-li zobrazit informace o daňovém rozdělení v souhrnech objednávek, zapněte zaškrtávací políčko **Zobrazit rozdělení daní v souhrnu objednávky**.  

Následující obrázek ukazuje zaškrtávací políčko **Zobrazit rozdělení daní v souhrnu objednávky** zvýrazněné a vybrané v konfigurátoru webu.

![Možnost Zobrazit rozdělení daní v souhrnu objednávky v konfigurátoru webu.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled DPH](/finance/general-ledger/indirect-taxes-overview)

[Konfigurace DPH pro online objednávky](sales-tax-config.md)

[Řešení potíží: Daně z online objednávek jsou nesprávně vypočítány](troubleshoot/tax-miscalculated-online-order.md)
