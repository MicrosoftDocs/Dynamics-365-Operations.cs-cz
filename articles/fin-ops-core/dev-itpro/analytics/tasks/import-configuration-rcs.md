---
title: (Elektronické výkaznictví) Import konfigurací z RSC
description: Toto téma obsahuje informace o tom, jak může uživatel importovat novou verzi konfigurace elektronického výkaznictví z RCS.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77d637b2ec1deeabc04a6796644363b330f5756e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744884"
---
# <a name="er-import-configurations-from-rcs"></a>(Elektronické výkaznictví) Import konfigurací z RSC

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Regulatory Configuration Services (RCS). V tomto příkladu vyberete verzi konfigurace elektronického výkaznictví, která byla nakonfigurována v instanci RCS, a importujte ji do aktuální instance pro vzorovou společnost, Litware, Inc. Tyto kroky lze provádět ve všech společnostech, protože konfigurace Felektronického výkaznictví je sdílena mezi společnostmi. K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). Chcete-li dokončit tento postup, musíte mít také přístup k instanci RCS, která obsahuje alespoň jednu konfiguraci elektronického výkaznictví ve stavu **dokončeno** nebo **sdíleno**.

1. Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**. 
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). 
3. Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, vyberte externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů pro zřízení RCS prostředí. 
4. Vyberte **Parametry elektronického výkaznictví**. 
5. Vyberte kartu **RCS**. 
6. Pokud jste již RCS prostředí pro vaši společnost zřídili, použijte pro přístup k ní uvedené adresy URL na stránce. 
7. Zavřete stránku. 

## <a name="register-a-new-er-repository"></a>Registrace nového úložiště elektronického výkaznictví 
1. Označte na seznamu vybraný řádek. 
2. Vyberte poskytovatele Litware, Inc. 
3. Vyberte Úložiště. 
4. Kliknutím na Přidat otevřete dialogové okno pro přetažení. 
5. V poli Typ úložiště konfigurace zadejte RCS. 
6. Zvolte Vytvořit úložiště. 
7. V poli zobrazovaného názvu prostředí RCS zadejte nebo vyberte hodnotu. 
8. Vyberte příslušnou instanci RCS. Můžete jich mít několik. 
9. Vyberte OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Import konfigurací elektronického z úložiště založeného na RCS
1. Vyberte **Zobrazit filtry**. 
2. Zadejte hodnotu filtru „RCS“ v poli **Název** za použití operátoru filtru **začíná na**. 
3. Po otevření vybraného úložiště na stránce **Připojit k Regulatory Configuration Services** vyberte odkaz **Zde vyberte pro připojení k Regulatory Configuration Services**. 
4. Zvolte **Otevřít**. 
5. Vyberte **Zavřít**. 
6. Vyberte požadovanou verzi konfigurace elektronického výkaznictví a výběrem možnosti **Import** ji převeďte do aktuální instance.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]