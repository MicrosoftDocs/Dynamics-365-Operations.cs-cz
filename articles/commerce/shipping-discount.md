---
title: Přepravní sleva
description: Tento článek popisuje možnosti přepravní slevy v Microsoft Dynamics 365 Commerce a nastavení, které je nutné k jejich použití.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346386"
---
# <a name="shipping-discount"></a>Přepravní sleva

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tento článek popisuje možnosti přepravní slevy v Microsoft Dynamics 365 Commerce a nastavení, které je nutné k jejich použití.

Doprava zdarma nebo se slevou je jedním z faktorů, který ovlivňuje rozhodování zákazníků o nákupu online. Aby zvýšili své tržby za transakci, mnoho maloobchodníků využívá výhodu dopravy zdarma, aby motivovali zákazníky ke zvýšení velikosti košíku.

Commerce podporuje možnost slevy na dopravu, která umožňuje maloobchodníkům nakonfigurovat procento slevy na poplatcích za dopravu pro konkrétní způsob dopravy, když celková částka prodeje za kvalifikované položky v transakci splňuje specifická kritéria. Příkladem scénáře, který využívá možnost slevy na dopravu, je „Utraťte $50 nebo více a získejte dopravu přes noc zdarma.“

## <a name="prerequisites"></a>Předpoklady

Možnost přepravní slevy je podporována funkcemi Commerce [Omnikanálové rozšířené automatické náklady](/dynamics365/unified-operations/retail/omni-auto-charges). Aby funkce slevy na dopravu fungovala, musíte povolit konfiguraci **Použít rozšířené automatické náklady** na kartě **Objednávky zákazníků** na stránce **Parametry Commerce** v Commerce headquarters. Maloobchodníci mohou využít funkci pokročilých automatických nákladů k nastavení různých typů poplatků, jako je manipulace, instalace a likvidace.

Přepravní slevy se vztahují pouze k poplatkům za dopravu. Prodejce proto musí specifikovat, které poplatky jsou poplatky za dopravu. Chcete-li určit poplatky za dopravu, přejděte v Commerce headquarters na **Nastavení kanálu \> Poplatky \> Kód poplatků** a nastavte možnost **Dopravné** na **Ano** pro požadované poplatky.

![Určení poplatku jako poplatku za dopravu.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfigurace

Možnost slevy na dopravu je založena na úrovních a podporuje pouze typ výpočtu **Procento slevy**. Chcete-li nastavit slevu na dopravu, přejděte v Commerce headquarters na **Ceny a slevy \> Mezní sleva expedice**. Poté můžete určit způsob dodání, na který se sleva vztahuje, definovat jednu nebo více prahových hodnot a nastavit procento slevy pro každou mezní hodnotu. Můžete také nakonfigurovat seznam kategorií nebo produktů jako kvalifikovaných položek. Tímto způsobem bude započítána pouze částka prodeje proti těmto položkám v transakci, když cenový modul vyhodnotí, zda celková částka transakce splňuje prahovou hodnotu.

> [!NOTE]
> Na rozdíl od jiných typů slev, sleva na dopravu nevytváří slevové řady. Místo toho přímo upraví poplatek za dopravu a k popisu poplatku připojí název slevy.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
