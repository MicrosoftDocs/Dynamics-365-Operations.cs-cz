---
title: Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce
description: Tohle téma vysvětluje, jak konfigurovat proces „nákup online, vyzvednutí v obchodě“ (BOPIS) ve zkušebním prostředí Microsoft Dynamics 365 Commerce po jeho zřízení.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71f2fb3882b51cdaed9b231cd605949195deca17
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213858"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurace BOPIS prostředí vyhodnocení aplikace Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tohle téma vysvětluje, jak konfigurovat proces „nákup online, vyzvednutí v obchodě“ (BOPIS) ve zkušebním prostředí Microsoft Dynamics 365 Commerce po zřízení tohoto prostředí.

## <a name="prerequisite"></a>Předpoklad

Postupy v tomto tématu dokončete až po zřízení a konfiguraci prostředí vyhodnocení Commerce verze Preview. Informace o zřízení a konfiguraci prostředí viz [Zřízení prostředí vyhodnocení aplikace Dynamics 365 Commerce](provisioning-guide.md) a [Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).

Po kompletním zřízení a konfiguraci prostředí Commerce můžete pomocí tohoto tématu povolit scénáře BOPIS.

## <a name="configure-the-pos"></a>Konfigurace POS

### <a name="configure-modern-pos"></a>Konfigurace Modern POS

Scénáře BOPIS, které zahrnují platbu kreditní kartou, vyžadují hardwarovou stanici. Hardwarová stanice je součástí klientů Modern POS pro Windows a Android. Používáte-li Cloud POS nebo Modern POS pro iOS, musí být pokladní místo (POS) spárováno se sdílenou hardwarovou stanicí. Toto téma vysvětluje, jak konfigurovat BOPIS pro klienty Windows a Android. Informace o nastavení sdílené hardwarové stanice viz [Konfigurace a instalace maloobchodní hardwarové stanice](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Přejděte na **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> Pokladny**.
2. Vyberte pokladnu **SANFRAN-5** a pak vyberte možnost **Upravit**.
3. Změňte hodnotu v poli **Hardwarový profil** z **HW002** na **HW001** a pak vyberte možnost **Uložit**.
4. Abyste změny synchronizovali, přejděte na **Retail a Commerce \> IT pro Retail a Commerce \> Plán distribuce**.
5. Vyberte plán distribuce **1090** a poté v podokně akcí vyberte možnost **Spustit**.
6. Vyberte možnost **Ano** a poté **OK**, abyste zahájili synchronizaci dat. 

### <a name="install-modern-pos"></a>Instalace Modern POS

1. Přejděte na **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> Zařízení**.
2. Vyberte zařízení **SANFRANCIS-5**.
3. V podokně akcí zvolte **Stáhnout** a poté vyberte **Konfigurační soubor**.
4. Vyberte možnost **Stáhnout** a pak možnost **Retail Modern POS**. 
5. Po stažení souboru **ModernPOSSetup.exe** vyberte možnost **Otevřít soubor**.

    ![Otevřít soubor](./dev-itpro/media/PAYMENTS/openfile.png)

6. Chcete-li projít instalačním procesem, vyberte možnost **Další**. Po dokončení instalace vyberte možnost **Zavřít**.

### <a name="activate-modern-pos"></a>Aktivace Modern POS

1. Na ploše systému Windows vyberte tlačítko **Start** a zadejte příkaz **Retail Modern POS**.
2. Vyberte aplikaci **Retail Modern POS**, která zahájí aktivaci.
3. Zvolte **Další**. Pole **Adresa URL serveru**, **ID zařízení** a **Číslo pokladny** by měla být přednastavena pomocí informací z konfiguračního souboru, který jste stáhli v předchozí proceduře.
4. Vyberte **Aktivovat**.
5. Zobrazí se dialogové okno ověření. Vyberte účet, který používá e-mailovou adresu, která byla dříve přidružena k pracovníkovi **000713 - Andrew Collette**.

    > [!NOTE]
    > Pokud jste pracovníka s vaší identitou ještě nevytvořili, nebude aktivace úspěšná. V takovém případě postupujte podle kroků v části „Přidružení pracovníka k vaší identitě“ v tématu [Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Když se zobrazí výzva k povolení správy zařízení vaší organizací, vyberte **Pouze tato aplikace**.
7. Po dokončení aktivace vyberte možnost **Začít**.

### <a name="enable-bopis-in-modern-pos"></a>Povolení BOPIS v Modern POS

1. Přihlaste se ke Modern POS s pomocí **000713** jako ID operátora a **123** jako hesla.
2. Když se přehrává úvodní návod, zaškrtněte obě políčka v levém dolním rohu dialogového okna a poté dialogové okno zavřete.
3. Nejste-li vyzváni k uzavření směny, posuňte se na **uvítací** stránce doprava, vyberte možnost **Zavřít směnu** a opět se přihlaste do POS.
4. Při výzvě vyberte možnost **Provést operace bez zásuvky**.
5. Na **uvítací** stránce se přesuňte doprava a vyberte operaci **Vybrat hardwarovou stanici**.
6. Vyberte **Spravovat**, nastavte možnost **Použít hardwarovou stanici** do polohy **Zapnuto** a poté klikněte na tlačítko **OK**.
7. Odhlaste se ze systému POS a znovu se přihlaste.
8. Po přihlášení vyberte možnost **Otevřít novou směnu** a pak vyberte možnost **Zásuvka**.

## <a name="complete-a-bopis-scenario"></a>Dokončení scénáře BOPIS

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Vytvoření objednávky výkladní skříně pro výdej na skladě

1. Přejděte na adresu URL, kterou jste zadali v kroku [Inicializace e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) během konfigurace prostředí.
2. Vyberte položku a vyberte možnost **Přidat do nákupního košíku**.
3. Na stránce nákupní tašky vyberte položku **Vyzvednout** pro řádek objednávky, který jste právě přidali.
4. V dialogovém okně **Vyberte úložiště** zadejte hodnotu **San Francisco** a pak vyberte tlačítko **Hledat**.
5. V seznamu výsledků vyhledejte úložiště San Francisco a vyberte **Vyzvednout zde**.
6. Na stránce nákupní tašky vyberte možnost **Přejít k pokladně jako host**. 

    > [!NOTE]
    > Chcete-li pokračovat k pokladně, je nutné potvrdit oznámení o souboru cookie. Toto oznámení je zobrazeno v pruhu v horní části stránky pokladny.

7. Pro metodu platby platební kartou zadejte následující údaje:

    - **Jméno držitele karty**: zadejte libovolné jméno.
    - **Číslo karty:** zadejte **4111-1111-1111-1111**.
    - **Datum vypršení platnosti:** zadejte **10/20**.
    - **Ověřovací hodnota platební karty (CVV)**: zadejte **737**.

    > [!IMPORTANT]
    > V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.

8. Pokračujte v placení zadáním fakturační adresy a pak vyberte možnost **Uložit a pokračovat**.
9. Jakmile bude objednávka připravena k podání, vyberte možnost **Pokladna**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Synchronizace online objednávek s administrativní podporou

Informace o synchronizaci online objednávek naleznete v tématu [Zaúčtování online prodeje a plateb](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).

### <a name="pick-up-an-order-in-the-store"></a>Vyzvednutí objednávky v obchodě

1. Přihlaste se k systému POS.
2. Na **úvodní** obrazovce vyberte možnost **Plnění objednávek**.
3. V seznamu položek pro výdej vyberte řádek z objednávky, která byla podána online.
4. Zatímco je vybrán řádek objednávky, vyberte možnost **Vyzvednout**.

    Položka řádku se přidá na obrazovku transakce a **$0,00** se zobrazí jako splatný zůstatek.

5. Vyberte splatný zůstatek **$0,00** nebo vyberte libovolný způsob platby k uzavření transakce.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Online objednávky načtené v POS mají nenulový splatný zůstatek.

Pokud je pro výdej v obchodě načtena objednávka, pokud splatné zůstatky nejsou 0 (nula), zkontrolujte, zda je používán Modern POS a zda je hardwarová stanice aktivní. Pokud používáte Cloud POS nebo Modern POS pro iOS, ujistěte se, že je sdílená hardwarová stanice aktivní. K načtení plateb, které byly provedeny v režimu online, je nutná nějaká forma aktivní hardwarové stanice.

### <a name="general-issues-with-payment-capture"></a>Obecné problémy se záznamem platby

V případě všech obecných problémů byste jako první věc měli vždy prostudovat protokoly událostí hardwarových stanic pro Modern POS nebo službu IIS (Internet Information Services). Tyto protokoly naleznete v následujících uzlech v protokolu událostí systému Windows:

- Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[Konektor platby Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Úspora nástrojů online plateb s konektorem Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Přehled omnikanálových plateb](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]