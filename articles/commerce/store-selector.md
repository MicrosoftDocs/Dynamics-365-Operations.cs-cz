---
title: Modul volby obchodu
description: Tento článek se zabývá modulem volby obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268312"
---
# <a name="store-selector-module"></a>Modul volby obchodu

[!include [banner](includes/banner.md)]

Tento článek se zabývá modulem volby obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Zákazníci mohou pomocí modulu pro výběr obchodu vyzvednout produkt ve vybraném obchodě po nákupu online. Ve verzi Commerce verze 10.0.13 obsahuje modul pro výběr obchodu také další funkce, které mohou zobrazit stránku **Najít obchod**, která zobrazuje obchody v okolí.

Modul pro výběr obchodu umožňuje uživatelům zadat umístění (město, stát, adresu atd.), aby vyhledávali obchody v okruhu hledání. Když je modul poprvé otevřen, použije k vyhledání obchodů umístění prohlížeče zákazníka (pokud je poskytnut souhlas).

## <a name="store-selector-module-usage"></a>Použití modulu volby obchodu

- Modul pro výběr obchodu lze použít na stránce s podrobnostmi o produktu (PDP) k výběru obchodu pro vyzvednutí.
- Modul pro výběr obchodu lze použít na stránce s košíkem k výběru obchodu pro vyzvednutí.
- Modul pro výběr obchodu lze použít na samostatné stránce, která zobrazuje všechny dostupné obchody.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Nastavení skupin plnění v centrále Commerce

Aby modul pro výběr obchodu zobrazil dostupné obchody, musí být v centrále Commerce nastavena skupina plnění. Další informace naleznete v tématu [Nastavení skupin plnění](customer-orders-overview.md#set-up-fulfillment-groups).

Kromě toho musí být pro každý obchod ve skupině plnění definována zeměpisná šířka a délka umístění úložiště v centrále.

Pro zadání hodnot zeměpisné šířky a délky umístění obchodu v centrále Commerce postupujte následovně.

1. Přejděte do části **Řízení zásob \> Nastavení \> Rozdělení zásob**.
1. V levém podokně vyberte umístění skladu.
1. Na rychlé kartě **Adresy** vyberte **Pokročilý**.

    ![Příklad podrobností obchodu v ústředí.](./media/Store-address.png)

1. V podokně akcí vyberte **Upravit**.
1. Na rychlé kartě **Všeobecné** zadejte hodnoty pro **Zeměpisná šířka** a **Zeměpisná délka**.

    ![Příklad nastavení zeměpisné šířky a délky pro obchod v centrále.](./media/Store-latitude-longitude.png)

1. V podokně akcí vyberte **Uložit**. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Skrýt obchod z modulu pro výběr obchodů

Některé obchody ve skupině plnění nemusí být platná místa vyzvednutí. Chcete-li zajistit, aby se jako možnosti v modulu pro výběr prodejny objevila pouze platná místa vyzvednutí, postupujte podle těchto kroků v Commerce headquarters.

1. Přejděte na **Retail a Commerce \> Nastavení Commerce \> Skupiny plnění \> Všechny obchody**.
1. V podokně akcí vyberte **Upravit**.
1. V **Nastavení** u každého obchodu, který není platným místem vyzvednutí, zrušte zaškrtnutí políčka **Je místo vyzvednutí**.
1. V podokně akcí vyberte **Uložit**.
1. Spusťte úlohu plánu distribuce 1070 **Konfigurace kanálu**.

## <a name="bing-maps-integration"></a>Integrace Bing Maps

Modul pro výběr obchodu je integrován do [Rozhraní pro programování aplikací Bing Maps REST (API)](/bingmaps/rest-services/), aby bylo možné používat funkce Geocoding a Autosuggestu společnosti Bing. Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky se sdílenými parametry pro centrálu Commerce. Geocoding API se používá k převodu polohy na hodnoty zeměpisné šířky a délky. Integrace s rozhraním Autosuggest API se používá k zobrazení návrhů vyhledávání, když uživatelé zadají umístění do vyhledávacího pole.

U rozhraní AUTOSuggest REST API musíte zajistit, aby byly povoleny následující adresy URL podle zásad zabezpečení obsahu vašeho webu (CSP). Toto nastavení se provádí v nástroji Commerce site Builder přidáním povolených adres URL do různých směrnic CSP pro web (například **img-src**). Další informace viz [Zásady zabezpečení obsahu](manage-csp.md). 

- Do směrnice **connect-src** přidejte **&#42;.bing.com**.
- Do směrnice **img-src** přidejte **&#42;.virtualearth.net**.
- Do směrnice **script-src** **přidejte &#42;.bing.com, &#42;.virtualearth.net**.
- Do směrnice **script-src** přidejte **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Režim Vyzvednutí v obchodě

Modul pro výběr obchodu podporuje a režim **Vyzvednutí v obchodě**, který zobrazuje seznam obchodů, kde je produkt k vyzvednutí. Ukazuje také provozní hodiny a inventář produktů pro každý obchod v seznamu. Modul selektoru obchodu vyžaduje, aby kontext produktu poskytoval dostupnost produktu a umožnil uživateli přidat produkt do košíku, pokud je režim dodání produktu nastaven na **vyzvednout** ve vybraném obchodě. Další informace naleznete v tématu [Nastavení zásob](inventory-settings.md). 

Modul volby obchodu lze přidat do modulu buy boxu na stránce v PDP, aby se zobrazily obchody, ve kterých je produkt k dispozici pro výdej. Lze jej také přidat do modulu košíku. V tomto případě modul pro výběr obchodu zobrazuje možnosti vyzvednutí pro každou položku řádku v košíku. Tento modul lze přidat na jiné stránky nebo do jiných modulů prostřednictvím rozšíření a přizpůsobení.

Aby scénář BOPIS fungoval, měly by být produkty konfigurovány se způsobem dodání **vyzvednutí zákazníkem**. V opačném případě se modul na příslušných stránkách produktu nezobrazí. Další informace o konfiguraci způsobu dodání naleznete v tématu [Nastavení způsobů dodání](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Následující obrázek znázorňuje příklad modulu volby obchodu použitého na stránce s podrobnostmi o produktu.

![Příklad modulu volby obchodu používaného u PDP.](./media/BOPIS.PNG)

> [!NOTE]
> Ve verzi 10.0.16 a novější lze povolit novou funkci, která organizaci umožňuje definovat více způsobů vyzvednutí zásilky pro zákazníky.  Pokud je tato funkce povolena, bude nástroj pro výběr obchodů a další moduly elektronického obchodování rozšířen, aby umožnil nakupujícímu vybrat si z potenciálně více možností vyzvednutí zásilky, pokud jsou nakonfigurovány.  Další informace o této funkci najdete v [této dokumentaci](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Najít režim obchodů

Modul pro výběr obchodu také podporuje režim **Najít obchody**. Tento režim lze použít k vytvoření stránky umístění obchodu, která zobrazuje dostupné obchody a jejich informace. V tomto režimu funguje modul pro výběr obchodu bez kontextu produktu a lze jej použít jako samostatný modul na jakékoli stránce webu. Kromě toho, pokud jsou pro modul zapnuta příslušná nastavení, uživatelé mohou vybrat obchod jako preferovaný. Je-li obchod vybrán jako preferovaný obchod uživatele, je ID obchodu udržováno v cookie prohlížeče. Proto musí uživatel přijmout zprávu o souhlasu s cookies.

Následující obrázek ukazuje příklad modulu pro výběr obchodu, který se používá společně s mapovým modulem na stránce umístění obchodu.

![Příklad modulu pro výběr obchodu a modulu mapování na stránce umístění obchodu.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Vykreslit mapu

Modul pro výběr obchodu lze spolu s mapovým modulem použít k zobrazení umístění obchodu na mapě. Další informace o modulu mapy naleznete v části [Modul galerie médií](map-module.md).

## <a name="store-selector-module-properties"></a>Vlastnosti modulu volby obchodu

| Název vlastnosti | Hodnota | popis |
|---------------|-------|-------------|
| Nadpis | Text | Nadpis modulu. |
| Režim | **Najít obchody** nebo **Vyzvednout v obchodě** | Režim **Najít obchody** zobrazuje dostupné obchody. Režim **Vyzvednout v obchodě** umožňuje uživatelům vybrat obchod pro vyzvednutí. |
| Styl | **Dialogové okno** nebo **Vložený** | Modul lze vykreslit buď jako vložený, nebo v dialogovém okně. |
| Nastavit jako preferovaný obchod | **Pravda** nebo **nepravda** | Když je tato vlastnost nastavena na **Pravda**, uživatelé mohou nastavit preferovaný obchod. Tato funkce vyžaduje, aby uživatelé přijali zprávu o souhlasu se soubory cookie. |
| Zobrazit všechny obchody | **Pravda** nebo **nepravda** | Když je tato vlastnost nastavena na **Pravda**, uživatelé mohou vynechat vlastnost **Poloměr vyhledávání** a zobrazit všechny obchody. |
| Možnosti automatického spuštění: Maximální výsledky | Počet | Tato vlastnost definuje maximální počet výsledků automatických návrhů, které lze zobrazit pomocí rozhraní Bing Autosuggest API. |
| Poloměr pro hledání | Počet | Tato vlastnost definuje poloměr při vyhledávání obchodů v mílích. Není-li zadána žádná hodnota, použije se výchozí poloměr 50 mil. |
| Podmínky služby | Adresa URL |  Tato vlastnost určuje podmínky adresy URL služby, která je vyžadována pro použití služby Mapy Bing. |

## <a name="site-settings"></a>Nastavení webu

Modul pro výběr obchodu respektuje [nastavení přidání produkt do košíku](add-cart-settings.md). Po přidání položky do košíku z modulu pro výběr obchodu se uživatelům webu zobrazí příslušné nakonfigurované pracovní postupy.

## <a name="add-a-store-selector-module-to-a-page"></a>Přidání modulu volby obchodu na stránku

Pro režim **Vyzvednutí v obchodě** lze modul použít pouze na PDP a na stránkách košíku. Režim musíte nastavit na **Vyzvednutí v obchodě** v podokně vlastností modulu.

- Informace o přidání modulu volby obchodu do modulu buy boxu naleznete v tématu [Modul buy boxu](add-buy-box.md). 
- Informace o přidání modulu volby obchodu do modulu košíku naleznete v tématu [Modul košíku](add-cart-module.md).

Chcete-li nakonfigurovat modul pro výběr úložiště tak, aby zobrazoval dostupné úložiště pro stránku umístění obchodu jako na obrázku, který byl zobrazen dříve v tomto článku, postupujte takto.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona marketingu** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Umístění obchodů** a poté vyberte **Další**.
1. V části **Vyberte šablonu** vyberte vytvořenou položku **Marketingová šablona** a poté vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Kontejner se 2 sloupci** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.
1. Nastavte hodnotu **Konfigurace portu s velmi malým zobrazením** na **100%**.
1. Nastavte hodnotu **Konfigurace portu s malým zobrazením** na **100%**.
1. Nastavte hodnotu **Konfigurace portu se středním zobrazením** na **33% 67%**.
1. Nastavte hodnotu **Konfigurace portu s velkým zobrazením** na **33% 67%**.
1. V pozici **Kontejner se 2 sloupci** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Výběr obchodů** a poté klikněte na **OK**.
1. V podokně vlastností modulu nastavte hodnotu **Režim** na **Najít obchody**.
1. Nastavte hodnotu v poli **Poloměr vyhledávání** v mílích.
1. Podle potřeby nastavte další vlastnosti, například **Nastavit jako preferovaný obchod**, **Zobrazit všechny obchody**, a **Povolit automatické návrhy**.
1. V pozici **Kontejner se 2 sloupci** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Mapa** a poté klikněte na **OK**.
1. V podokně vlastností modulu nastavte podle potřeby další vlastnosti.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
 
## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Rychlá prohlídka stránky podrobností o produktu](quick-tour-pdp.md)

[Rychlá prohlídka košíku a pokladny](quick-tour-cart-checkout.md)

[Nastavit způsoby dodání](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Správa map Bing pro vaši organizaci](dev-itpro/manage-bing-maps.md)

[Rozhraní REST API Map Bing](/bingmaps/rest-services/)

[Modul Mapy](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
