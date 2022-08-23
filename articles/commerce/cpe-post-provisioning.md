---
title: Konfigurace sandboxového prostředí Dynamics 365 Commerce
description: Tento článek vysvětluje, jak konfigurovat sandboxové prostředí Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270339"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Konfigurace sandboxového prostředí Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak konfigurovat sandboxové prostředí Microsoft Dynamics 365 Commerce poté, co je zřízeno.

Postupy v tomto článku dokončete až po zřízení sandboxového prostředí Commerce. Informace o postupu zřízení sandboxového prostředí Commerce najdete v části [Zřízení sandboxového prostředí Commerce](provisioning-guide.md).

Po kompletním zřízení sandboxového prostředí Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít používat prostředí. K dokončení těchto kroků je nutné použít prostředí Lifecycle Services (LCS) Microsoft Dynamics a Dynamics 365 Commerce.

## <a name="before-you-start"></a>Než začnete

1. Přihlaste se do [portálu LCS](https://lcs.dynamics.com).
1. Přejděte na svůj projekt.
1. V seznamu vyberte své prostředí.
1. V informacích o prostředí vpravo vyberte **Přihlášení k prostředí**. Budete posláni do centrály Commerce.
1. Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**. Tato právnická osoba byla předem nakonfigurována v ukázkových datech.
1. Přejděte na **Parametry Commerce \> Konfigurační parametry** a zkontrolujte, že záznam **ProductSearch.UseAzureSearch** existuje a je nastaven na **true**. Pokud tato položka chybí, přidejte ji a nastavte hodnotu na **true**.
1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Inicializovat plánovač obchodu**. V plovoucí nabídce **Inicializovat plánovač obchodu** nastavte možnost **Odstranit existující konfiguraci** na **Ano** a pak vyberte **OK**.
1. Aby kanály obchodu a elektronického obchodu správně fungovaly, musí být přidány do Commerce Scale Unit. Přejděte na **Maloobchod a obchod \> Nastavení centrály \> Plánovač obchodu \> Databáze kanálů** a pak v levém podokně vyberte Commerce Scale Unit. Na pevné záložce **Maloobchodní kanál** přidejte kanály **Internetový obchod AW**, **Internetový obchod AW Business** a **Rozšířený internetový obchod Fabrikam**, pokud plánujete používat tyto kanály elektronického obchodování. Volitelně můžete také přidat maloobchodní prodejny, pokud budete používat pokladní místo (POS) (např. **Seattle**, **San Francisco** a/nebo **San Jose**).
1. Chcete-li zajistit, aby byly všechny změny synchronizovány s databází kanálů, vyberte **Databáze kanálů \> Úplná synchronizace dat** pro Commerce Scale Unit..

Během činností po zřízení v centrále Commerce se ujistěte, že právnická osoba **USRT** je vždy vybrána.

## <a name="configure-the-point-of-sale"></a>Konfigurace pokladního místa

### <a name="associate-a-worker-with-your-identity"></a>Přidružení pracovníka k vaší identitě

Chcete-li pracovníka s vaší identitou přidružit, postupujte následovně v centrále Commerce.

1. Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Zaměstnanci \> Pracovníci**.
1. V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**. Tento vzorový uživatel je přidružen k obchodu v San Franciscu, který bude použit v další sekci.
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

## <a name="set-up-your-e-commerce-sites"></a>Nastavení webů elektronického obchodování

K dispozici jsou tři dostupné demo stránky elektronického obchodování: Fabrikam, Adventure Works a Adventure Works Business. Při konfiguraci každého ukázkového webu postupujte podle následujících kroků.

1. Přihlaste se k nástroji pro tvorbu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Vyberte web (**Fabrikam**, **Adventure Works** nebo **Adventure Works Business**) a otevřete dialogové okno nastavení webu.
1. Vyberte doménu, kterou jste zadali při inicializaci Commerce.
1. V centrále vyberte předkonfigurovaný kanál internetového obchodu (**Rozšířený internetový obchod Fabrikam**, **Internetový obchod AW** nebo **Internetový obchod AW Business**), který odpovídá výchozímu kanálu.
1. Jako výchozí jazyk vyberte **en-us**.
1. Nakonfigurujte pole cesty. Toto může být ponecháno prázdné pro jeden web, ale pokud používáte stejný název domény pro více webů, bude nutné jej nakonfigurovat. Například, pokud je název domény `https://www.constoso.com`, můžete použít prázdnou cestu pro Fabrikam (`https://contoso.com`) a poté použít "aw" pro Adventure Works (`https://contoso.com/aw`) a „awbusiness“ pro obchodní web Adventure Works (`https://contoso.com/awbusiness`).
1. Vyberte **OK**. Zobrazí se seznam stránek na webu.
1. Volitelně opakujte kroky 2-7 pro konfiguraci dalších ukázkových webů podle potřeby.

## <a name="enable-jobs"></a>Povolit úlohy

Pokud chcete povolit úlohy v Commerce, postupujte takto:

1. Přihlaste se k prostředí centrály.
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

Po dokončení postupu zřizování a konfigurace můžete začít používat sandboxové prostředí. Pomocí adresy URL nástroje pro tvorbu webu Commerce můžete přejít na práci s vytvářením. Pomocí adresy URL webu Commerce přejděte do prostředí webu zákazníka maloobchodu.

Pokud chcete provést konfiguraci volitelných funkcí sandboxového prostředí Commerce, najdete informace v části [konfigurace volitelných funkcí sandboxového prostředí Commerce](cpe-optional-features.md).

Chcete-li uživatelům elektronického obchodu umožnit přihlášení k webu elektronického obchodu, je vyžadována další konfigurace umožňující ověření webu prostřednictvím Azure Active Directory business-to-consumer (B2C). Pokyny naleznete v [Nastavení klienta B2C v Commerce](set-up-b2c-tenant.md).

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

[Zřízení sandboxového prostředí Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurace volitelných funkcí pro sandboxové prostředí Dynamics 365 Commerce](cpe-optional-features.md)

[Konfigurace BOPIS v sandboxovém prostředí Dynamics 365 Commerce](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
