---
title: Vytvoření a aktualizace pracovní doby obchodu
description: V tomto článku je popsán postup při vytváření a aktualizaci pracovní doby obchodu v programu Commerce Headquarters.
author: josaw1
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 99d2f06be959e00656901c6ca8fc79fac32a3a6f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884358"
---
# <a name="create-and-update-store-hours"></a>Vytvoření a aktualizace pracovní doby obchodu

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Přehled

Z jednoho místa mohou maloobchodní prodejci vytvářet, spravovat a řídit pracovní doby obchodu pro různé obchody napříč geografickými oblastmi. Pracovní doby obchodu lze poté zobrazit na terminálech na pokladním místě (POS). Tímto způsobem mohou pokladní uživatelé sdílet pracovní doby obchodu se zákazníky a pomoci nakupujícím, kteří mají zájem o zásoby v jiných obchodech. Pracovní doby obchodu lze rovněž vytisknout na účtenky v případě, že se odběratelé chtějí vrátit do obchodu později.

Více pracovních dob obchodu lze konfigurovat napříč různými kanály. Tyto kanály zahrnují kamenné obchody, kontaktní střediska, mobilní zařízení a weby s elektronickým obchodováním.

Pokud má odběratel objednávku výdeje pro jiný obchod, může pokladník vybrat data, kdy bude výdej v daném obchodě k dispozici. Vyhledávání obchodu poskytne odkaz na data a pracovní doby obchodu. Pokladník může vybrat datum a místo a také můžete vytisknout příjemku odběru, která zahrnuje pracovní dobu obchodu.

Tato funkce je k dispozici v Microsoft Dynamics 365 Retail verze 8.1.2 a novější.

## <a name="configure-store-hours"></a>Konfigurace pracovní doby obchodu

Chcete-li nakonfigurovat pracovní dobu obchodu, postupujte následovně.

1. Přejděte na **Retail a Commerce** \> **Nastavení kanálu** \> **Pracovní doba obchodu**.
2. Vyberte **Nová** pro vytvoření nové šablony pracovní doby obchodu. Chcete-li použít existující šablonu, vyberte ji v levém podokně.
3. V dialogovém okně **Přidat rozsah** definujte rozsah dat, pracovní dobu obchodu a všechny požadované svátky.

    - Pokud se pracovní doba obchodu nezmění, vyberte **Nikdy nekončí** v poli **Koncové datum**.
    - Pokud je pracovní doba obchodu pro určitý měsíc, týden nebo den, nastavte příslušná data v polích **Počáteční datum** a **Koncové datum**.

    > [!NOTE]
    > Je možné vytvořit více šablon, které se překrývají s počátečním a koncovým datem. Lze tedy například definovat pracovní dobu obchodu pro obchody v různých časových pásmech.

    ![Dialogové okno Přidat rozsah.](../dev-itpro/media/Storehours1.png "Dialogové okno Přidat rozsah")

4. Přiřaďte k šabloně pracovní doby obchodu obchody, kde bude použita. V dialogovém okně **Vybrat uzly organizace** vyberte obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.

    - Ke každému obchodu lze přidružit pouze jednu šablonu pracovní doby obchodu.
    - Pomocí tlačítek se šipkami vyberte obchody, regiony nebo organizace. Kalendář bude k dispozici pro obchody nebo skupiny obchodů a bude viditelný na POS pro referenci.

    ![Dialogové okno Vybrat organizační uzly.](../dev-itpro/media/Storehours2.png "Dialogové okno Vybrat organizační uzly")

5. Na stránce **Plán distribuce** spusťte úlohy **1070** a **1090**, které umožní POS zpřístupnit pracovní dobu.

## <a name="add-store-hours-to-printed-receipts"></a>Přidat pracovní dobu obchodu do vytištěných účtenek

Pomocí následujících kroků přidejte do tištěných příjemek POS pracovní dobu obchodu.

1. Otevřete návrhář formátu příjemky.
2. V levém dolním rohu vyberte možnost **Zápatí**.
3. Přetáhněte prvek **Pracovní doba obchodu** z levého podokna do zápatí v dolní části šablony účtenky.
4. Můžete upravit výchozí popisek v prvku **Pracovní doba obchodu** podle potřeby.
5. Uložte příjemku a zavřete návrhář účtenky.
6. Na stránce **Plán distribuce** spusťte úlohy **1070** a **1090**.
7. Přihlaste se k systému POS.
8. Dokončete prodej a vyberte Tisk účtenky.

Příjemky POS nyní zahrnují pracovní dobu obchodu. Pokud byly do šablony zahrnuty nějaké svátky, zobrazí se na účtence.

![Příklad účtenky.](../dev-itpro/media/Storehours3.png "Příklad účtenky")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]