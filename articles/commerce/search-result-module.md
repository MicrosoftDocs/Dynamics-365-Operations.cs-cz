---
title: Modul výsledků hledání
description: Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919467"
---
# <a name="search-results-module"></a>Modul výsledků hledání

[!include [banner](includes/banner.md)]


Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul výsledků vyhledávání vrátí výsledky vyhledávání produktů a seznam příslušných zpřesnění pro produkty. Moduly výsledků hledání na webech Dynamics 365 Commerce lze použít k vykreslení stránek pro následující scénáře:

- Výsledky vyhledávání, které jsou spuštěny vyhledáváním uživatelů
- Výsledky vyhledávání, které zobrazují konkrétní sadu produktů, například „Nakupujte podobný vzhled“
- Seznamy produktů, které patří do kategorie

Další informace o kategoriích a stránkách s výsledky vyhledávání najdete v části [Výchozí cílová stránka kategorie a přehled stránky s výsledky vyhledávání](category-search-page-overview.md).

Následující obrázek ukazuje příklad stránky výsledků hledání pro kategorii na webu Fabrikam.

![Příklad stránky výsledků vyhledávání na webu Fabrikam.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Vlastnosti modulu výsledků hledání

V následující tabulce jsou uvedeny vlastnosti modulů výsledků hledání spolu s jejich hodnotami a popisy.

| Vlastnost | Hodnoty | popis |
|----------|--------|-------------|
| Počet položek na stránku | Celé číslo | Počet položek, které by měly být zobrazeny na každé stránce. |
| Povolit zpět na PDP | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, když uživatel vybere produkt na stránce s výsledky vyhledávání, navigace s popisem cesty na stránce s podrobnostmi o produktu (PDP), která je otevřena, zobrazí odkaz „Zpět na výsledky“. |
| Rozbalit zpřesnění | **Všechno**, **1**, **2**, **3** nebo **4** | Počet nejlepších upřesnění, které by se měly při načtení stránky rozšířit. Například, pokud je tato vlastnost nastavena na **3**, budou rozbaleny první tři upřesnění na stránce. |
| Skrýt zobrazení hierarchie kategorií | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, zobrazení hierarchie kategorií na stránce bude skryto. Tato vlastnost by měla být nastavena na **True**, pokud používáte [modul popisu cesty](add-breadcrumb.md) pro zobrazení hierarchie kategorií.|
| Zahrnout do výsledků vyhledávání atributy produktu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, budou vráceny atributy produktů ve výsledcích hledání. Ačkoli tyto atributy lze zobrazit na webu Commerce, je nutné rozšíření.|
| Zobrazit ceny na pobočkách | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, ceny umístění pro produkty se zobrazí ve výsledcích vyhledávání, když přihlášený uživatel prochází stránku. |
| Aktualizujte panel zpřesnění | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, panel zpřesnění bude aktualizován, jakmile budou vybrána zpřesnění. V tomto režimu se některá zpřesnění s vícenásobným výběrem budou při aktualizaci panelu zpřesnění chovat jako zpřesnění s jedním výběrem. |

> [!IMPORTANT]
> V Commerce verze 10.0.16 a novější lze konfiguraci **Zobrazit ceny umístění** použít k zobrazení cen umístění na stránce.
>
> Ve verzi Commerce verze 10.0.20 a novějších lze konfiguraci **Aktualizujte panel zpřesnění** použít k aktualizaci panelu zpřesnění během výběru zpřesnění.

## <a name="supported-modules"></a>Podporované moduly

Modul výsledků vyhledávání podporuje [modul rychlého zobrazení](quick-view-module.md), který umožňuje uživatelům prohlížet informace o produktu a přidávat položky do košíku ze stránky výsledků vyhledávání.

## <a name="add-a-search-results-module-to-a-category-page"></a>Přidat modul výsledků vyhledávání na stránku kategorie

Chcete-li přidat modul výsledků vyhledávání na stránku kategorie, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** zadejte název **Výsledků vyhledávání** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (...) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Popis cesty** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Popis cesty** zadejte hodnotu **1** pro **Min. počet výskytů**.
1. V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výsledky vyhledávání** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Výsledky vyhledávání** zadejte hodnotu **1** pro **Min. počet výskytů** a poté nastavte další požadované vlastnosti modulu výsledků hledání. Nastavením těchto vlastností v šabloně zajistíte, že veškerá přizpůsobení konkrétní stránce kategorie budou tato nastavení automaticky zahrnovat.
1. Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Výsledky vyhledávání**, kterou jste vytvořili, zadejte **Stránku kategorie** pro **Název stranky** a pak vyberte tlačítko **OK**. Protože jsou všechny hodnoty nastaveny v šabloně, je stránka připravena k publikování.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Povolit povědomí o zásobách pro modul výsledků vyhledávání

Zákazníci obecně očekávají, že web elektronického obchodu bude po celou dobu procházení informován o zásobách, takže se mohou rozhodnout, co dělat, pokud pro produkt neexistuje žádný inventář. Modul výsledků vyhledávání lze vylepšit tak, aby zahrnoval data inventáře a poskytoval následující možnosti:

- Spolu s produkty zobrazte štítek dostupnosti inventáře.
- Skrýt produkty, které nejsou skladem.
- Zobrazit produkty, které nejsou skladem, na konci seznamu výsledků vyhledávání.
    
Chcete-li povolit tato prostředí, musíte nakonfigurovat následující nastavení nezbytných předpokladů v centrále Commerce.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Aktivace funkce Vylepšené zjišťování produktů elektronického obchodování s ohledem na zásoby

> [!NOTE]
> Funkce **Vylepšené zjišťování produktů v elektronického obchodování s ohledem na zásoby** je k dispozici od verze Commerce 10.0.20.

Chcete-li povolit funkci **Vylepšené zjišťování produktů v elektronického obchodování s ohledem na zásoby** v ústředí Commerce, postupujte takto.

1. Přejděte na **Pracovní prostory \> Správa funkcí**.
1. Vyhledejte funkci **Vylepšené zjišťování produktů elektronického obchodování s ohledem na zásoby** a aktivujte ji.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigurace úlohy Naplnění atributů produktu úrovní zásob

Úloha **Naplnění atributů produktu úrovní zásob** vytvoří nový atribut produktu pro zachycení dostupnosti zásob a poté tento atribut nastaví na nejnovější hodnotu úrovně zásob pro každý hlavní produkt. Protože se dostupnost zásob prodávaného produktu nebo sortimentu neustále mění, důrazně doporučujeme naplánovat úlohu jako dávkový proces.

Chcete-li nakonfigurovat úlohu **Naplnění atributů produktu úrovní zásob:** centrále Commerce, postupujte takto.

1. Přejděte na **Retail a Commerce \> Retail a Commerce IT \> Produkty a zásoby**.
1. Vyberte **Naplnění atributů produktu úrovní zásob**.
1. V dialogovém okně **Naplnění atributů produktu úrovní zásob** postupujte takto:

    1. V části **Parametry** v poli **Atribut produktu a název typu** zadejte název vyhrazeného atributu produktu, který bude vytvořen pro zachycení dostupnosti zásob.
    1. V části **Parametry** v poli **Dostupnost zásob na základě** vyberte množství, na kterém by měl být založen výpočet úrovně zásob (např. **Dostupné fyzické**).
    1. V části **Spustit na pozadí** nakonfigurujte úlohu tak, aby se spouštěla na pozadí, a volitelně zapněte možnost **Dávkové zpracování**. 

> [!NOTE]
> Pro konzistentní výpočet úrovně zásob napříč PDP a stránkami se seznamem produktů na vašem webu elektronického obchodu nezapomeňte vybrat stejnou možnost množství pro nastavení **Dostupnost zásob na základě** v centrále Commerce i nastavení **Úroveň zásob na základě** v nástroji Commerce Site Builder. Další informace o nastavení zásob v tvůrci webů naleznete v části [Použití nastavení zásob](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Konfigurace nového atributu produktu

Po spuštění úlohy **Naplnění atributů produktu úrovní zásob** musíte nakonfigurovat nově vytvořený atribut produktu na webu elektronického obchodu, kde chcete povolit přehled o zásobách pro modul výsledků vyhledávání.

Ke konfiguraci atributu nového produktu v centrále Commerce postupujte následovně.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu** a vyberte web elektronického obchodování.
1. Vyberte a otevřete přidruženou skupinu atributů, přidejte do ní nově vytvořený atribut produktu a poté stránku zavřete.
1. Vyberte **Nastavit metadata atributu**, vyberte nově přidaný atribut produktu a poté zapněte možnosti **Zobrazit atribut na kanálu**, **Načítatelné**, **Lze zpřesnit** a **Lze se dotázat**.

> [!NOTE]
> U produktů, které se zobrazují v modulu výsledků vyhledávání, se úroveň zásob zadává na úrovni hlavního produktu namísto úrovně jednotlivých variant. Má pouze dvě možné hodnoty: „na skladě“ a „není na skladě“. Samotný text hodnot je načten z definice [profil úrovně zásob](inventory-buffers-levels.md). Hlavní produkt je považován za vyprodaný pouze v případě, že nejsou skladem všechny jeho varianty. Úroveň zásob varianty je určena na základě definice profilu úrovně zásob produktu. 

Po dokončení všech předchozích konfiguračních kroků zobrazí zpřesňující parametry na stránkách s výsledky vyhledávání filtr založený na inventáři a modul výsledků vyhledávání načte data inventáře ze zákulisí. Poté můžete nakonfigurovat **Nastavení zásob pro stránky se seznamem produktů** v nástroji Commerce Site Builder, abyste mohli ovládat, jak modul výsledků vyhledávání zobrazuje produkty, které nejsou skladem. Další informace [Použít nastavení zásob](inventory-settings.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul rychlého zobrazení](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
