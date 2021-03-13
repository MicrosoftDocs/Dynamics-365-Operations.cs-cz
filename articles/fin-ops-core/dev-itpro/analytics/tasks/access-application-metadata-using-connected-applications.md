---
title: Přístup k metadatům aplikace pomocí připojených aplikací
description: Kroky v tomto tématu vysvětlují, jak může uživatel služby Regulatory Configuration Service navrhnout nové mapování modelu elektronického výkaznictví (ER) pomocí metadat.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457d5760fb704b7a93ce16c081b7c5e6d0ff19c1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093323"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Přístup k metadatům aplikace pomocí připojených aplikací

[!include [banner](../../includes/banner.md)]

Následující kroky vysvětlují, jak může uživatel služby Regulatory Configuration Service s rolí Správce systému nebo Návrhář elektronického výkaznictví navrhnout nové mapování modelu elektronického výkaznictví (ER) pomocí metadat v aplikaci Finance and Operations. Přístup k metadatům aplikace bude probíhat online pomocí aplikace připojené k RCS. Mapování modelu ER bude konfigurováno pro přístup k transakcím zahraničního obchodu. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). Pokud jste nedokončili kroky uvedené v tématu [Přístup k metadatům aplikace pomocí konfigurace ER](access-application-metadata-er-configuration.md), přejděte na stránku [Příklady elektronického výkaznictví](https://go.microsoft.com/fwlink/?linkid=862266) a stáhněte a uložte následující konfigurace ER: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml a dokončete kroky v postupu.

## <a name="prerequisites"></a>Předpoklady
1. Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**. 
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Získání požadovaných konfigurací ER
1. Klikněte na **Konfigurace výkaznictví**. 
2. Pokud jste již provedli kroky v části [Přístup k metadatům aplikace pomocí konfigurace ER](access-application-metadata-er-configuration.md), již máte v aktuální instanci RCS všechny potřebné konfigurace ER (konfigurace metadat pro zahraniční obchod, model a mapování). Zbývající kroky tohoto dílčího úkolu můžete vynechat. 
3. Klikněte na **Exchange**. 
4. Klikněte na **Načíst ze souboru XML**. 
5. Klikněte na **Procházet** a vyberte soubor **Foreign trade metadata.xml**. 
6. Klikněte na tlačítko **OK**. 
7. Klikněte na **Exchange**. 
8. Klikněte na **Načíst ze souboru XML**. 
9. Klikněte na **Procházet** a vyberte soubor **Foreign trade model.xml**. 
10. Klikněte na tlačítko **OK**. 
11. Klikněte na **Exchange**. 
12. Klikněte na **Načíst ze souboru XML**. 
13. Klikněte na **Procházet** a vyberte soubor **Foreign trade mapping.xml**. 
14. Klikněte na tlačítko **OK**. 

## <a name="register-a-connected-application"></a>Registrace připojené aplikace
1. Zavřete stránku. 
2. Zavřete stránku. 
3. Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**. 
4. Klikněte na **Připojené aplikace**. 
5. Ujistěte se, že konfigurovaná aplikace založená na Azure založena a přístupná pro aktuálního uživatele RCS. Rovněž je nutné, aby aktuální uživatel RCS měl přístup k vybrané aplikaci a byl zaregistrován jako uživatel této aplikace, který má roli poskytující oprávnění pro přístup k metadatům aplikace. 
6. Klepněte na možnost **Nový**. 
7. Do pole **Název** zadejte 'MyConnectedApp'. 
8. Do pole **Aplikace** zadejte https:// mycompany.operations.dynamics.com. 
9. Do pole **Klient** zadejte ‘mycompany.onmicrosoft.com’. 
10. Klikněte na možnost **Uložit**. 
11. Při kontrole připojení ke konfigurované aplikaci klikněte na stránce **Připojit ke vzdálené aplikaci na** odkaz **Kliknutím sem se připojte k vybrané aplikaci**. 
12. Klikněte na **Zkontrolovat připojení**. 
13. Klepněte na tlačítko **Zavřít**. 
14. Po úspěšném ověření připojení budou podrobnosti o verzi a tenantu aktualizovány pro konfigurovanou aplikaci v aktuální mřížce. 

## <a name="review-existing-model-mapping-configuration"></a>Kontrola existující konfigurace mapování modelu ER
1. Zavřete stránku. 
2. Klikněte na **Konfigurace výkaznictví**. 
3. Ve stromovém zobrazení rozbalte **Zahraniční obchodní model**. 
4. Ve stromové struktuře vyberte **Model zahraničního obchodu\Mapování zahraničního obchodu**. 
5. Rozbalte oddíl **Předpoklady**. 

    > [!NOTE]
    > V současné době toto mapování odkazuje na konfiguraci metadat. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo. 

6. Klikněte na možnost **Návrhář**. 
7. Klikněte na možnost **Návrhář**. 
8. Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**. 
9. Klikněte na možnost **Přidat kořen**. 
10. V poli **Tabulka** zadejte nebo vyberte hodnotu. 

    > [!NOTE]
    > V současné době toto mapování odkazuje na konfiguraci metadat. Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo. 

11. Klepněte na možnost **Zrušit**. 
12. Zavřete stránku. 
13. Zavřete stránku. 

## <a name="assign-connected-application-to-model-mapping"></a>Přiřazení připojené aplikace k mapování modelu 
1. Klikněte na možnost **Upravit**. 
2. Vyberte aplikaci **MyConnectedApp**. 

    > [!NOTE]
    > V současné době toto mapování odkazuje na metadata vybrané připojené aplikace. Pokud stejné mapování odkazuje na konfiguraci metadat a připojenou aplikaci současně, budou použita metadata připojené aplikace. 

3. Klikněte na možnost **Návrhář**. 
4. Klikněte na možnost **Návrhář**. 
5. Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**. 
6. Klikněte na možnost **Přidat kořen**. 
7. V poli **Tabulka** zadejte nebo vyberte hodnotu. 

    > [!NOTE]
    > Nyní byly nabídnuty více než dvě tabulky aplikace, protože toto mapování používá všechna metadata připojené aplikace, která je k ní přiřazena. 

8. Klepněte na možnost **Zrušit**. 
9. Klikněte na tlačítko **Ověřit**. 

    > [!NOTE]
    > Úspěšně jste provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat připojené aplikace, která byla přiřazena pro toto mapování. 

10. Zavřete stránku. 
11. Zavřete stránku. 

Potřebujete-li vyhodnotit mapování modelu pomocí metadat jiné verze aplikace, zaregistrujte jinou připojenou aplikaci, přiřaďte ji k tomuto mapování modelu a ověřte ji proti novým metadatům.
