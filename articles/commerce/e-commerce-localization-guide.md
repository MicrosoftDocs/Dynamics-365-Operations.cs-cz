---
title: Průvodce lokalizací elektronického obchodu Dynamics 365 Commerce
description: Tento článek popisuje, jak lokalizovat web elektronického obchodu Microsoft Dynamics 365 Commerce do dalších jazyků a konfigurovat web tak, aby podporoval více kanálů.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873377"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Průvodce lokalizací elektronického obchodu Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak lokalizovat web elektronického obchodu Microsoft Dynamics 365 Commerce do dalších jazyků a konfigurovat web tak, aby podporovaly více kanálů. Najdete tu také koncepty a terminologii související s procesem.

Schopnosti elektronického obchodování v Dynamics 365 Commerce byly navrženy tak, aby aktivovaly online prostředí, které lze přizpůsobit konkrétním zemím a jazykům, ale zároveň umožňují maximální opětovné použití šablon, stránek, obsahu a médií. Můžete také vytvořit základní web a poté expandovat na nové trhy přidáním podpory pro další země a jazyky v průběhu času.

## <a name="definitions"></a>Definice

**Národní prostředí, identifikátor národního prostředí**: Národní prostředí (také známé jako identifikátor národního prostředí) definuje jazyk, který je přidružen k zemi nebo oblasti. Například identifikátor národního prostředí "fr-ca" je spojen s kanadskou francouzštinou.

**Základní jazyk** : Jazyk, ve kterém vyvíjíte obsah webu, než jej exportujete pro lokalizaci.

**Kanál, internetový obchod**: Kanál (známý také jako internetový obchod) definuje platební metody, cenové skupiny, hierarchie produktů, sortimenty a produkty pro výkladní skříň online elektronického obchodu.

## <a name="concepts"></a>Koncepty

### <a name="url-driven-experience"></a>Prostředí řízené adresou URL

Weby elektronického obchodu Dynamics 365 Commerce poskytují zákazníkům jedinečné marketingové a lokalizované prostředí vytvářené prostřednictvím kanálů a identifikátorů národního prostředí. Kanály definují jedinečné produkty, kategorie, měny a platební metody pro daný trh a identifikátory národního prostředí určují jazyk obsahu, který zákazníci uvidí. Web elektronického obchodu používá adresy URL k rozlišení mezi marketingovým a lokalizovaným prostředím. Adresy URL webu pro tyto jedinečné kanály a prostředí jsou pro web definovány ve stránce **Nastavení webu \> Kanály** v konfigurátoru webů Dynamics 365 Commerce.

V konfigurátoru webu je adresa URL kombinací domény a cesty, která definuje vstupní bod pro jedinečnou kombinaci kanálu a národního prostředí. V následujícím příkladu fiktivní internetový obchod s názvem Fabrikam Inc. definuje čtyři jedinečné kombinace kanálu a národního prostředí a mapuje každou kombinaci na jedinečnou adresu URL, která poskytuje obsah zákazníkům.

| Doména                     |  Cesta      | Kanál       |   Národní prostředí     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Rozšířený internetový obchod Fabrikam | cs  |
| `https://fabrikam.com` | /es    | Rozšířený internetový obchod Fabrikam | es     |
| `https://fabrikam.ca`  | /      | Online obchod Contoso    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Online obchod Contoso    | en-ca  |

#### <a name="domain"></a>Doména

Domény se zakládají, když si založíte web elektronického obchodu ve službách Microsoft Dynamics Lifecycle Services (LCS). Po zřízení vašeho prostředí elektronického obchodu můžete přidat další domény otevřením požadavku na službu. Další informace o nastavení domén pro web elektronického obchodu najdete v článku [Domény v Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Cesta

- Cesta je libovolný řetězec, který je v kombinaci s doménou mapován na jedinečnou kombinaci kanálu a národního prostředí. V předchozím příkladu se řetězec, který je použit jako cesta, shoduje s identifikátorem národního prostředí, na který je cesta mapována. Můžete však použít jiný přístup.
- Kombinace kanálu a národního prostředí může být mapována na doménu a prázdnou cestu ("/"). V předchozím příkladu zákazníci, kteří navštíví adresu `https://fabrikam.ca/`, získají produkty a sortiment pro kanadský trh v kanadské francouzštině.
- Konfigurátor webu Commerce vám brání ve vytváření duplicitních kombinací domény a cesty. Můžete však mapovat duplicitní kombinace kanálu a národního prostředí na jinou kombinaci domény a cesty.

#### <a name="channel"></a>Kanál

- Kanály (známé také jako online obchody) definují platební metody, cenové skupiny, hierarchie produktů, sortimenty a produkty pro výkladní skříň online elektronického obchodu.
- Kanály jsou definovány, konfigurovány a publikovány v centrále Dynamics 365 Commerce.
- Konfigurátor webu může detekovat online obchody, které byly konfigurovány v centrále Commerce a je možné je mapovat na web.

Další informace o kanálech naleznete v tématu nápovědy [Přehled kanálů](channels-overview.md). Další informace o tom, jak nastavit online kanál, najdete v článku [Nastavení online kanálu](channel-setup-online.md).

#### <a name="locale"></a>Národní prostředí

- Národní prostředí je skutečný identifikátor používaný při předávání souborů ve formátu XLIFF (XML Localization Interchange File Format) k lokalizaci. Národní prostředí jsou definována a publikována pro každý kanál v centrále Commerce. Informace o tom, jak konfigurovat jazyky a kanály v nástroji pro tvorbu webu, najdete v další části.
- Stejné národní prostředí lze mapovat na více kanálů. Tímto způsobem může být na více trzích nabízen společný jazyk.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Konfigurace jazyků a kanálů pro web elektronického obchodu

Ve výchozím nastavení jsou všechny weby elektronického obchodu Dynamics 365 Commerce konfigurovány tak, aby používaly jeden online kanál a jeden jazyk, bez ohledu na to, zda začnete s ukázkovým webem Fabrikam nebo vytvoříte nový web od začátku.

V této konfiguraci zákazníci a partneři obvykle vyvíjejí všechny materiály, které budou používány v různých zemích a jazycích. Tyto materiály zahrnují šablony, stránky, fragmenty, obsah a média. Veškerý obsah webu je vyvíjen v prvním jazyce, který jste pro svůj web vybrali, nebo pokud používáte ukázkový web Fabrikam, bude obsah webu vyvíjen v angličtině.

![Výchozí nastavení webu elektronického obchodu Dynamics 365 Commerce](media/loc-guide-1.png)

> [!NOTE]
> V ukázkovém web Fabrikam můžete konfigurovat další jazyk, aby bylo možné vývoj obsahu provádět v tomto jazyce. Informace o tom, jak přidat nový jazyk do webu a kanálu najdete v části [Konfigurace dalšího jazyka pro web](#configure-an-additional-language-for-your-site) dále v tomto článku.

Nicméně systém správy obsahu (CMS) a model stránky pro weby elektronického obchodu Dynamics 365 Commerce byly navrženy tak, aby umožňovaly expanzi na nové trhy a lokality. Proto můžete prostřednictvím jediného webu elektronického obchodu spravovat materiály pro internetový obchod pokrývající více trhů a jazyků.

![Web elektronického obchodu Dynamics 365 Commerce, který pokrývá několik trhů a jazyků](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Konfigurace dalšího jazyka pro web

Proces konfigurace nového jazyka pro web elektronického obchodu má tři kroky.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Krok 1: Přidejte jazyk do svého kanálu (online obchodu) v centrále Commerce

1. V centrále Commerce přejděte na kanál, do kterého chcete přidat nový jazyk. Chcete-li najít seznam online obchodů, které jsou nakonfigurovány v centrále Commerce, přejděte na **Maloobchod a obchod \> Kanály \> Online obchody**.
1. Otevřete internetový obchod, který je namapován na váš web, výběrem jeho **ID maloobchodního kanálu**. Internetový obchod, který je namapován na váš web, můžete ověřit otevřením stránky nastavení webu **Kanály** v konfigurátoru webů Commerce a přečtením názvu ve sloupci **Kanály**. 
1. Na záložce s náhledem **Jazyky** vyberte **Přidat**. V poli **Jazyk** vyberte kód národního prostředí pro nový jazyk. Pak vyberte **Uložit**.
1. Až budete hotovi, přejděte na **Maloobchod a velkoobchod \> IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu **Konfigurace kanálu 1070**. Po dokončení úlohy můžete přejít ke kroku 2 a přidat v konfigurátoru webu jazyk do kanálu pro váš web.

![Záložka Jazyky online obchodu v centrále Commerce](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Krok 2: Přidejte jazyk do kanálu v konfigurátoru webu

Chcete-li v konfigurátoru webu přidat jazyk do kanálu, postupujte podle následujících kroků.

1. V konfigurátoru webů Commerce otevřete web a poté otevřete stránku **Kanály** v nastavení webu.
1. Vyberte název kanálu, do kterého chcete přidat jazyk.
1. V pravém podokně vyberte **Přidat národní prostředí**.
1. V dialogu **Přidat národní prostředí** v části **Přidat národní prostředí** vyberte národní prostředí pro jazyk, který jste dříve přidali do kanálu v ústředí Commerce.
1. Vyberte doménu a cestu, kterou budou zákazníci zadávat, aby mohli zobrazit váš web v tomto kanálu a jazyce.
1. Pokud chcete, aby byl jazyk výchozím jazykem pro prohlížení, vytváření a aktualizaci stránek a fragmentů konfigurátoru webu, zapněte políčko **Použít jako výchozí jazyk autorského kanálu**. 
    > [!NOTE]
    > Toto nastavení ovlivňuje pouze konfigurátor webu. Nemá vliv na web publikovaný pro vaše zákazníky.
1. Vyberte **OK**.
1. Vyberte možnost **Uložit a publikovat**.

#### <a name="step-3-localize-your-site-content"></a>Krok 3: Lokalizujte obsah svého webu

Když se vrátíte do zobrazení **Stránky** v konfigurátoru webů Commerce, nový jazyk bude k dispozici v ovládacím prvku výběru kanálu a národního prostředí vpravo nahoře. Nyní můžete vytvářet lokalizované verze stránek ve vašem základním jazyce.

Proces lokalizace obsahu vašich stránek a fragmentů je popsán v části [Lokalizace obsahu webu elektronického obchodu](#localize-e-commerce-site-content) dále v tomto článku.

### <a name="configure-a-new-channel-for-your-site"></a>Konfigurace nového kanálu pro web

Weby elektronického obchodování Dynamics 365 Commerce mohou poskytovat prostředí, která jsou definována v několika online kanálech konfigurovaných v centrále Commerce. Web používá několik kanálů, aby zákazníkům ukázal jedinečnou konfiguraci platebních metod, cenových skupin, hierarchie produktů, sortimentu a sady produktů. Kanál se obvykle používá ke konfiguraci těchto dimenzí tak, aby vyhovovaly požadavkům a preferencím pro prostředí, které je spojeno s jednotlivými zeměmi. Tento přístup je však obchodním rozhodnutím zákazníka. Není to nutnost.

Předpoklady a úkoly spojené s nastavením kanálu (online obchodu) jsou nad rámec tohoto dokumentu. Další informace o tom, jak nastavit online kanál v centrále Commerce, najdete v článku [Základy nastavení kanálu](channels-overview.md#channel-setup-basics). Informace o krocích a požadavcích specifických pro online kanály najdete v tématu [Nastavení online kanálu](channel-setup-online.md).

Chcete-li v konfigurátoru webu přidat kanál do webu, postupujte podle následujících kroků.

1. V konfigurátoru webů Commerce přejděte do nabídky **Nastavení webu \> Kanály**. 
1. Vyberte **Přidat kanál**.
1. V dialogu **Přidat kanál** v části **Kanál** vyberte kanál, který chcete přidat. 
    > [!NOTE]
    > Můžete přidat pouze kanály, které ještě do webu nebyly přidány.
1. Vyberte výchozí národní prostředí pro kanál. Pokud do kanálu přidáte nové jazyky, můžete změnit výchozí jazyk na jeden z nich.
1. Zadejte doménu a cestu, která bude tvořit adresu URL, která poskytuje obsah a prostředí pro tuto kombinaci kanálu a jazyka.
1. Vyberte **OK**.
1. Vyberte možnost **Uložit a publikovat**.

## <a name="localize-e-commerce-site-content"></a>Lokalizace obsahu webu elektronického obchodu

### <a name="xliff-basics"></a>Základy formátu XLIFF

XLIFF je standardní průmyslový formát souborů pro předávání lokalizovatelného obsahu mezi nástroji pro správu obsahu. Konfigurátor webů Commerce používá formát souboru XLIFF k exportu obsahu stránek, fragmentů a metadat obrázků, takže je lze lokalizovat a znovu importovat.

Zákazníci používající Microsoft Dynamics obvykle spolupracují s dodavateli lokalizace třetích stran, jako jsou např. [Translated.com](https://translated.com/welcome), pro překlad souborů XLIFF do jazyků, které potřebují.

### <a name="localize-assets-in-site-builder"></a>Lokalizace materiálů v konfigurátoru webu

V konfigurátoru webu lze lokalizovat následující materiály webu elektronického obchodu:

- Stránky
- Fragmenty
- Multimediální materiály
- Moduly

Všechny nové stránky, fragmenty a multimediální materiály jsou vytvářeny v kontextu kanálu a jazyka, které jsou aktuálně vybrány ve výběru kanálu a národního prostředí. Tento jazyk je obvykle vaším „základním jazykem“, pokud jste nekonfigurovali další jazyky nebo kanály. Na webech, kde je konfigurováno více kanálů a jazyků, je „základní jazyk“ definován kanálem a národním prostředím, které jste nastavili jako výchozí na stránce **Kanály** v nastavení webu.

Kroky lokalizace obsahu pro stránky, fragmenty a mediální materiály jsou podobné. Na výjimky a rozdíly upozorníme v následujících částech. Kroky při lokalizaci obsahu modulu se však liší. Více informací naleznete v části [Lokalizace modulů](#localize-modules) dále v tomto článku.

#### <a name="step-1-export-an-xliff-file"></a>Krok 1: Exportujte soubor XLIFF

Chcete-li exportovat soubor XLIFF pro stránku, fragment nebo obrázek v nástroji pro tvorbu webu, postupujte takto.

1. Otevřete materiál, pro který chcete exportovat obsah základního jazyka, aby jej bylo možné lokalizovat.
1. Na panelu příkazů vyberte příkaz **Lokalizace \> Export XLIFF**.
    > [!NOTE]
    > Možnost **Lokalizace** je viditelná pouze tehdy, když je materiál ve stavu **Upravit**.

Soubor XLIFF s názvem **\<assetname\> .xlf** bude stažen do složky stažených souborů vašeho prohlížeče. Tento soubor XLIFF je specifický pro materiál, který lokalizujete. Exportujte soubor XLIFF pro každý materiál, který chcete lokalizovat.

#### <a name="step-2-localize-the-xliff-file"></a>Krok 2: Lokalizujte soubor XLIFF

Ve většině případů budete při překladu souborů XLIFF spolupracovat s dodavatelem lokalizace. Pokud však lokalizujete materiály interně nebo pokud chcete proces lokalizace pouze otestovat, musíte v souboru XLIFF provést následující změny:

- Přidejte atribut cílového jazyka do prvku /xliff/file a nastavte jeho hodnotu na identifikátor národního prostředí jazyka, do kterého provádíte lokalizaci. 
    > [!NOTE]
    > Tento identifikátor národního prostředí se musí shodovat s identifikátorem národního prostředí ze stránky **Kanály** v nastavení webu.
- Pro každý prvek //source přidejte cílový prvek na stejné úrovni, kde textová hodnota je lokalizovaná verze obsahu tohoto zdrojového prvku.

Informace o schématu, kterým se řídí soubory XLIFF, naleznete v článku [Specifikace XLIFF 1.2](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Chcete-li materiál lokalizovat do více jazyků, musíte pro každý z těchto jazyků vytvořit lokalizovaný soubor XLIFF.

#### <a name="step-3-import-the-localized-xliff-file"></a>Krok 3: Importujte lokalizovaný soubor XLIFF

Chcete-li importovat soubor XLIFF pro materiál, postupujte takto.

1. V konfigurátoru webů Commerce otevřete materiál, pro který chcete importovat soubor XLIFF.
1. V ovládacím prvku výběru kanálu a národního prostředí v pravém horním rohu vyberte kanál a jazyk, pro který importujete lokalizovaný obsah.
1. Na panelu příkazů vyberte příkaz **Lokalizace \> Import XLIFF**. Poté vyhledejte a vyberte lokalizovaný soubor XLIFF pro vybraný materiál a jazyk.

Po úspěšném importu souboru XLIFF se vytvoří „varianta“ stránky, fragmentu nebo materiálu. Od tohoto okamžiku budou všechny změny provedené v lokalizované variantě ovlivňovat pouze tuto variantu. Neovlivní základní materiál, ze kterého byla varianta odvozena. Stejně tak změny základního materiálu neovlivní variantu tohoto materiálu. 

V případě stránek však můžete provádět změny napříč variantami úpravou šablony nebo rozvržení, ke kterému jsou tyto stránky vázány. Obdobně změny fragmentu ovlivní všechny stránky, které jsou na dané variantě závislé.

### <a name="images"></a>Obrázky

Obrázky lze vykreslit ve variantě stránky nebo modulu pouze v případě, že jsou lokalizována metadata obsahu, která jsou s těmito obrázky spojena. V současné době lze lokalizovat následující metadata v multimediálním materiálu:

- Alternativní text
- Popis
- Titul

V současné době nemůžete lokalizovat binární soubor digitálního materiálu, jako je obrázek nebo video. Produktový tým Dynamics 365 Commerce v současné době na této schopnosti pracuje.

### <a name="localize-modules"></a>Lokalizace modulů

Řetězce, které jsou vypsány jako součást samotného modulu (například „Předchozí“ a „Další“ v modulu karuselu), jsou lokalizovány odděleně od obsahu modulu. Pokyny najdete v tématu [Lokalizace modulu](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Další prostředky

[Glosář modelu stránky](page-elements-overview.md)

[Sdílení napříč kanály](cross-channel-sharing.md)

[Lokalizace modulu](e-commerce-extensibility/localize-module.md)

[Soubor definice modulu](e-commerce-extensibility/module-definition-file.md)

[Lokalizace zdrojů rozšíření Commerce a souborů popisků](dev-itpro/extension-resource-localization.md)

[Globalizace modulů pomocí třídy CultureInfoFormatter](e-commerce-extensibility/globalize-modules.md)

[Nastavení aplikace: Motivy](e-commerce-extensibility/app-settings.md#themes-section)
