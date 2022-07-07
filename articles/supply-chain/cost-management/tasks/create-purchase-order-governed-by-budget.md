---
title: Vytvoření nákupní objednávky řízené rozpočtem
description: Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016181"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Vytvoření nákupní objednávky řízené rozpočtem

[!include [banner](../../includes/banner.md)]

Pomocí tohoto postupu lze vytvořit nákupní objednávku, u které proběhne kontrola dostupného rozpočtu.

## <a name="review-the-budget-control-configuration"></a>Zkontrolujte konfiguraci kontroly rozpočtu

1. Přejděte na **Rozpočtování > Nastavení > Kontrola rozpočtu > Konfigurace kontroly rozpočtu**.
1. Vyberte kartu **Dostupné rozpočtové prostředky**.
1. Vyberte kartu **Dokumenty a deníky**.
1. Vyberte kartu **Definovat pravidla kontroly rozpočtu**.
1. Vyberte kartu **Definovat rozpočtové skupiny**.
1. Zavřete stránku.

## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte do nabídky **Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**.
1. Zvolte **Nové**.
1. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
1. Rozbalte pevnou záložku **Obecné**.
1. Do pole **Datum účtování** nastavte datum.
1. Vyberte **OK** dialogové okno se zavře a nová prodejní objednávka se otevře.
1. Na pevné záložce **Řádky nákupní objednávky** vyberte **Přidat řádek** z panelu nástrojů a přidejte nový řádek a poté řádek vyplňte podle potřeby pro přidání položky do objednávky.
1. Na panelu nástrojů pevné záložky **Řádky nákupní objednávky** vyberte **Finance \> Distribuce částek**.
1. Do pole **Účet hlavní knihy** zadejte účet.
1. Zavřete stránku.

## <a name="perform-budget-checking"></a>Provést kontrolu rozpočtu

1. Pokračujte v práci s nákupní objednávkou, do které jste právě přidali řádek.
1. Na panelu nástrojů pevné záložky **Řádky nákupní objednávky** vyberte **Finance \> Provést kontrolu rozpočtu**.
1. Na panelu nástrojů pevné záložky **Řádky nákupní objednávky** vyberte **Finance \> Chyby a varování kontroly rozpočtu**.
1. Otevře se dialog **Chyby a varování kontroly rozpočtu**. Zkontrolujte výsledky kontroly a poté vyberte **Zavřít** pro uzavření dialogu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]