---
title: Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Tento článek vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 19d88139e35554bce68bc6203141957b96e439a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892323"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.

Postupy v tomto článku dokončete až po zřízení prostředí vyhodnocení Commerce. Informace o postupu zřízení prostředí vyhodnocení Commerce najdete v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).

Po kompletním zřízení prostředí vyhodnocení Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít posuzovat prostředí. K dokončení těchto kroků je nutné použít prostředí Lifecycle Services (LCS) Microsoft Dynamics a Dynamics 365 Commerce.

## <a name="before-you-start"></a>Než začnete

1. Přihlaste se do [portálu LCS](https://lcs.dynamics.com).
1. Přejděte na svůj projekt.
1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. V informacích o prostředí vpravo vyberte **Přihlášení k prostředí**. Budete posláni do centrály Commerce.
1. Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**.
1. Přejděte na **Parametry Commerce \> Konfigurační parametry** a zkontrolujte, že záznam **ProductSearch.UseAzureSearch** existuje a je nastaven na **true**. Pokud tato položka chybí, můžete ji přidat, nastavit hodnotu na **true** a poté vybrat příkaz **Databáze kanálů \> Úplná synchronizace dat** pro Commerce Scale Unit spojenou s vaším webem elektronického obchodu.
1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Inicializovat plánovač obchodu**. V plovoucí nabídce **Inicializovat plánovač obchodu** nastavte možnost **Odstranit existující konfiguraci** na **Ano** a pak vyberte **OK**.
1. Chcete-li přidat kanály do jednotky Commerce Scale Unit, přejděte na **Maloobchod a obchod \> Nastavení centrály \> Plánovač obchodu \> Databáze kanálů** a poté v levém podokně vyberte jednotku Commerce Scale Unit. Na pevné záložce **Maloobchodní kanál** přidejte kanály **Internetový obchod AW**, **Internetový obchod AW Business** a **Rozšířený internetový obchod Fabrikam**. Volitelně můžete také přidat maloobchodní prodejny, pokud budete používat POS (např. **Seattle**, **San Francisco** a **San Jose**).

Během činností po zřízení v centrále Commerce se ujistěte, že právnická osoba **USRT** je vždy vybrána.

## <a name="configure-the-point-of-sale"></a>Konfigurace pokladního místa

### <a name="associate-a-worker-with-your-identity"></a>Přidružení pracovníka k vaší identitě

Chcete-li pracovníka s vaší identitou přidružit, postupujte následovně v centrále Commerce.

1. Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Zaměstnanci \> Pracovníci**.
1. V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**.
1. V podokně akcí klikněte na možnost **Commerce**.
1. Vyberte **Stávající identita přidružení**.
1. Do pole **E-mail** vpravo od **Hledání pomocí e-mailu** zadejte svou e-mailovou adresu.
1. Vyberte **Vyhledat**.
1. Vyberte záznam obsahující vaše jméno.
1. Vyberte **OK**.
1. Zvolte **Uložit**.

### <a name="activate-cloud-pos"></a>Aktivovat Cloud POS

Chcete-li aktivovat Cloud POS, postupujte následovně v LCS.

1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. V informacích o prostředí vpravo vyberte **Přihlášení ke cloudovému pokladnímu místu**.
1. Vyberte **Další**, chcete-li otevřít dialogové okno **Než začneš**.
1. Nechte pole **Adresa URL serveru** tak, jak je. Zvolte **Další**.
1. Přihlaste se pomocí účtu Microsoft Azure Active Directory (Azure AD).
1. Pro **Jméno obchodu** vyberte **San Francisco** a poté vyberte **Další**.
1. V **Registr a zařízení** vyberte **SANFRAN-1**.
1. Vyberte **Aktivovat**. Jste přihlášeni a přesměrováni na přihlašovací stránku POS.
1. Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátora **000713** a hesla **123**.

## <a name="set-up-your-site-in-commerce"></a>Nastavení webu v Commerce

Pokud chcete začít nastavovat web vyhodnocení v Commerce, postupujte následovně.

1. Přihlaste se k nástroji pro tvorbu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Vyberte web **Fabrikam** otevřete dialogové okno nastavení webu.
1. Vyberte doménu, kterou jste zadali při inicializaci platformy e-Commerce.
1. Jako výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**. (Zkontrolujte, zda jste vybrali **rozšířený** online obchod.)
1. Jako výchozí jazyk vyberte **en-us**.
1. Ponechte hodnotu pole **Cesta** tak, jak je.
1. Vyberte **OK**. Zobrazí se seznam stránek na webu.
1. Opakujte kroky 2-7 pro web **AdventureWorks** (který se mapuje na kanál **Internetový obchod AW**) a web **AdventureWorks Business** (který se mapuje na kanál **Internetový obchod AW Business**). Pokud je pole **Cesta** pro web Fabrikam prázdné, musíte přidat cesty ke dvěma webům AdventureWorks (například „aw“ a „awbusiness“).

## <a name="enable-jobs"></a>Povolit úlohy

Pokud chcete povolit úlohy v Commerce, postupujte takto:

1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky vlevo přejděte na **Retail and commerce \> Dotazy a sestavy \> Dávkové úlohy**.

    Zbývající kroky tohoto postupu musí být dokončeny pro každou z následujících úloh:

    * Zpracovat maloobchodní oznámení objednávky e-mailem
    * Dostupnost produktu
    * P-0001
    * Synchronizovat úlohu objednávek

1. Pomocí rychlého filtru vyhledejte úlohu podle názvu.
1. Je-li stav úlohy nastaven na **Probíhající**, postupujte následovně:

    1. Vybrat záznam.
    1. V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.
    1. Vyberte **Ruší se** a poté vyberte **OK**.

1. Je-li stav úlohy nastaven na **Sraženo**, postupujte následovně:

    1. Vybrat záznam.
    1. V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.
    1. Vyberte možnost **Čekání** a potom **OK**.

Volitelně můžete také nastavit interval opakování na jednu (1) minutu pro následující úlohy:

* Zpracovat úlohu maloobchodního oznámení objednávky e-mailem
* úloha P-0001
* Synchronizovat úlohu objednávek

### <a name="run-full-data-synchronization"></a>Spustit úplnou synchronizaci dat

Chcete-li spustit úplnou synchronizaci dat v Commerce, postupujte takto v centrále Commerce.

1. Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálů**.
1. Vyberte kanál, který je nazvaný **scXXXXXXXXX**.
1. V podokně akcí vyberte **Úplná synchronizace dat**.
1. Jako plán distribuce zadejte **9999**.
1. Vyberte **OK**.
1. Vyberte **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testování informací o kreditní kartě za účelem provedení zkušebních nákupů

Chcete-li provést zkušební transakce na webu, můžete použít následující testovací kreditní kartu:

- **Číslo karty:** 4111-1111-1111-1111
- **Datum konce platnosti:** 10/30
- **Ověřovací hodnota platební karty (CVV):** 737

> [!IMPORTANT]
> V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.

## <a name="next-steps"></a>Další kroky

Po dokončení postupu zřizování a konfigurace můžete začít používat prostředí vyhodnocení. Pomocí adresy URL nástroje pro tvorbu webu Commerce můžete přejít na práci s vytvářením. Pomocí adresy URL webu Commerce přejděte do prostředí webu zákazníka maloobchodu.

Pokud chcete provést konfiguraci volitelných funkcí prostředí vyhodnocení Commerce, najdete informace v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).

> [!NOTE]
> Prostředí vyhodnocení Commerce přicházejí s předinstalovaným klientem Azure Active Directory (Azure AD) business-to-consumer (B2C) pro demonstrační účely. Konfiguace vlastního klienta Azure AD B2C není potřeba pro prostředí vyhodnocení. Pokud však konfigurujete zkušební prostředí tak, aby používalo vašeho vlastního klienta Azure AD B2C, nezapomeňte přidat ``https://login.commerce.dynamics.com/_msdyn365/authresp`` jako URL pro odpověď v aplikaci Azure AD B2C přes Azure Portal.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Seznam kanálů nástroje Site Builder je při konfiguraci webu prázdný

Pokud nástroj pro tvorbu webu nezobrazuje žádné kanály online obchodu, zkontrolujte v centrále, že kanály byly přidány do jednotky Commerce Scale Unit, jak je popsáno v sekci [Než začnete](#before-you-start) výše. Spusťte také úlohu **Inicializovat plánovač obchodu** s polem **Odstranit stávající konfiguraci** nastaveným na **Ano**.  Jakmile jsou tyto kroky dokončeny, spusťte ve stránce **Databáze kanálů** (**Maloobchod a obchod\> Nastavení centrály \> Obchodní plánovač \> Databáze kanálů**) úlohu **9999** na jednotce Commerce Scale Unit.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Vzorníky barev se nevykreslují na stránce kategorie, ale vykreslují se na stránce s podrobnostmi o produktu (PDP)

Následujícím postupem zajistěte, aby vzorky barev a velikostí byly nastaveny tak, aby je bylo možné upravit.

1. V centrále přejděte na **Maloobchod a obchod \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. V levém podokně vyberte kanál internetového obchodu a poté vyberte **Nastavit metadata atributu**.
1. Nastavte možnost **Zobrazit atribut na kanálu** na **Ano**, nastavte možnost **Lze upřesnit** na **Ano** a poté vyberte **Uložit**. 
1. Vraťte se na stránku kanálu internetového obchodu a poté vyberte **Publikovat aktualizace kanálu**.
1. Přejděte na **Maloobchod a obchod \> Nastavení centrály \> Plánovač obchodu \> Databáze kanálů** a spusťte úlohu **9999** na jednotce Commerce Scale Unit.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Zdá se, že obchodní funkce nejsou na webu AdventureWorks zapnuté

V centrále se ujistěte, že kanál internetového obchodu má **Typ zákazníka** nastaven na **B2B**. Pokud je **Typ zákazníka** nastaven na **B2C**, musí být vytvořen nový kanál, protože stávající kanál nelze upravovat. 

Ukázková data dodávaná ve verzi Commerce 10.0.26 a dřívějších verzích obsahovala chybnou konfiguraci kanálu **Internetový obchod AW Business**. Řešením je vytvořit nový kanál se stejným nastavením a konfiguracemi s výjimkou **Typu zákazníka**, který by měla být nastaven na **B2B**.

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Zřízení prostředí vyhodnocení Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
