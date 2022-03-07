---
title: Částečná dodávka nákladu přepravy
description: Toto téma vysvětluje, jak můžete částečně expedovat vytížení a odložení plánování vytížení kapacity.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 5ea844531314b4dd2ff3fa46d8f0b57d9c47059e684d677f06f8259b264d4a90
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782292"
---
# <a name="partial-shipment-of-a-transport-load"></a>Částečná dodávka nákladu přepravy

[!include[banner](../includes/banner.md)]

Nastavením částečné dodávky náklady lze zpracovat náklady, kde kapacitu nelze určit, dokud nebudou všechny řádky prodeje přidány k nákladu. Proces pak může být dokončen, když je známý přesný počet palet. Z tohoto důvodu není nutné rozhodnout, které palety budou přiřazeny ke kterému přenosu až do okamžiku, kdy je přeprava fyzicky nakládána mimo fázované zásoby.

Tato funkce je alternativou dodržování pevnější struktury, kde je třeba určit, které palety budou přiřazeny které přepravě před vyskladněním nebo nakládkou. Uživatelé mohou místo toho nakonfigurovat jednotlivé náklady pro potvrzení částečné dodávky. Poté mohou být provedeny přepravy pro tyto náklady. Proto může oddělení plánování přepravy plánovat náklady, aniž by musely zohlednit kapacitu jednotlivých přeprav.

V době nakládky mohou pracovníci definovat novou zátěž přepravy, na kterou lze paletu naložit. Případně mohou identifikovat stávající náklad přepravy. Tato data lze zaznamenat pomocí mobilního zařízení. Několik pracovníků skladu proto může naložit zásob ze stejných nebo různých nákladů na stejnou dodávku. Náklady lze poté úplně nebo částečně expedovat.

> [!NOTE] 
> Aby bylo možné naložit zásoby z nakládky do konkrétní přepravní nakládky a nakládku částečně expedovat, je nutné vygenerovat práci pomocí třídy nakládky v pracovní šabloně. Běžná práce výdeje typu **výdej** nelze naložit pro přepravu, například na dodávku.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Nastavení nakládek pro přepravu částečných dodávek

Nastavení nakládek pro přepravu částečných dodávek se skládá z následujících postupů.

### <a name="set-the-loading-strategy"></a>Nastavení strategie vytížení

Je nutné povolit částečnou nakládku nastavením strategie nakládky. Po vytvoření nakládky můžete nastavit strategii nakládání.

1. Vyberte **řízení skladu** \> **Nakládky** \> **Všechny nakládky**.
2. Vyberte nakládku a klikněte na **záhlaví**.
3. V poli **Strategie nakládky** vyberte **Povolena částečná nakládka**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Vytvoření položky nabídky pro nakládku pro přepravu

Je nutné vytvořit novou položku nabídky, která umožňuje dopravovat náklady, které mají být naloženy. Nakládka pro přepravu umožňuje seskupit pracovní řádky z jedné nebo několika nakládek. Vše, co je přidáno k přepravní nakládce, pak lze expedovat pomocí mobilního skeneru.

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.
2. Vyberte **Nový** a poté v poli **Režim** vyberte **Práce**.
3. Nastavte hodnotu možnosti **Použít stávající práci** na **Ano**.
4. Na kartě **Obecné** v poli **Směřuje** vyberte **Nakládka pro přepravu**.
5. Pro povolení potvrzení expedice na snímače mobilního zařízení v poli **Povolený typ potvrzení expedice** vyberte **Přeprava nákladu**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Potvrdit expedici přepravy nákladu z klienta

Toto nastavení umožňuje potvrdit expedici nákladu obsahující úplný náklad nebo částečný náklad.

1. Vyberte **řízení skladu** \> **Nakládky** \> **Přeprava nakládky**.
2. V podokně akcí na kartě **Expedovat a přijmout** ve skupině **Potvrdit** vyberte **Přeprava**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]