---
title: Modul výsledků hledání
description: Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/21/2022
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
ms.openlocfilehash: 15b3bb50eb0b75fa19ac8e136da83cb362b4cec6
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644919"
---
# <a name="search-results-module"></a>Modul výsledků hledání

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

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

Zákazníci obecně očekávají, že web elektronického obchodu bude po celou dobu procházení informován o zásobách, takže se mohou rozhodnout, co dělat, pokud pro produkt neexistuje žádný inventář. Modul výsledků vyhledávání lze konfigurovat tak, aby zahrnoval data inventáře a poskytoval následující možnosti:

- Spolu s produkty zobrazte štítek dostupnosti zásob.
- Skryjte produkty, které nejsou skladem, v seznamu produktů.
- Zobrazte produkty, které nejsou skladem, na konci seznamu výsledků vyhledávání.
- Filtrujte produkty ve výsledcích vyhledávání podle úrovně inventáře.

Chcete-li povolit tyto funkce, musíte nejprve povolit funkci **Vylepšené zjišťování produktů v e-commerce, abyste byli informováni o zásobách** v pracovním prostoru **Správa funkcí**.

> [!NOTE]
> Funkce **Vylepšené zjišťování produktů v elektronického obchodování s ohledem na zásoby** je k dispozici od verze Commerce 10.0.20 a novějších verzích.

Vyhledávání produktů s ohledem na zásoby používá atributy produktů k získání informací o dostupnosti zásob. Nezbytným předpokladem této funkce je vytvoření vyhrazených atributů produktu, zadání dat o zásobách a jejich přidání do online kanálu. 

Chcete-li vytvořit vyhrazené atributy produktu pro podporu modulu výsledků vyhledávání s ohledem na skladové zásoby, postupujte takto.

1. Přejděte na **Retail a Commerce \> Retail a Commerce IT \> Produkty a zásoby**.
1. Vyberte a otevřete **Naplnění atributů produktu úrovní zásob**.
1. V dialogovém okně zadejte následující informace:

    1. V poli **Název atributu a typu produktu** zadejte název vyhrazeného atributu produktu, který bude vytvořen pro zachycení dostupnosti zásob.
    1. V poli Parametry v poli **Dostupnost zásob na základě** vyberte typ množství, na kterém by měl být založen výpočet úrovně zásob (např. **Dostupné fyzické**). 

1. Spusťte úlohu na pozadí. Vzhledem k tomu, že se zásoby produktů ve vícekanálovém prostředí neustále mění, důrazně doporučujeme naplánovat tuto úlohu jako dávkový proces.

> [!NOTE]
> Pro konzistentní výpočet úrovně zásob napříč stránkami a modly se seznamem produktů na vašem webu elektronického obchodu nezapomeňte vybrat stejnou možnost množství pro nastavení **Dostupnost zásob na základě** v centrále Commerce i nastavení **Úroveň zásob na základě** v nástroji Commerce Site Builder. Další informace o nastavení zásob v tvůrci webů naleznete v části [Použití nastavení zásob](inventory-settings.md).

Chcete-li nakonfigurovat atributy produktu pro online kanál, postupujte takto. 

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
2. Vyberte online kanál, pro který chcete povolit modul výsledků vyhledávání s ohledem na zásoby.
3. Vyberte a otevřete přidruženou skupinu atributů a přidejte do ní nově vytvořený atribut produktu.
4. Pro verze služby Commerce před vydáním verze 10.0.27 vyberte **Nastavit metadata atributu**, vyberte nově přidaný atribut produktu a poté zapněte možnosti **Zobrazit atribut na kanálu**, **Načítatelné**, **Lze zpřesnit** a **Lze se dotázat**.
5. Až budete hotovi, přejděte na **Maloobchod a velkoobchod \> IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu **Konfigurace kanálu 1150 (katalog)**. Pokud naplánujete úlohu **Naplnit atributy produktu úrovní zásob** jako dávkový proces, doporučujeme také naplánovat úlohu 1150 jako dávkový proces, který běží se stejnou frekvencí.

> [!NOTE]
> U produktů, které se zobrazují v modulu výsledků vyhledávání, se úroveň zásob ukazuje na úrovni hlavního produktu namísto úrovně jednotlivých variant. Má pouze dvě možné hodnoty: „na skladě“ a „není na skladě“. Skutečný popisek hodnoty je načten z definice [profil úrovně zásob](inventory-buffers-levels.md). Hlavní produkt je považován za vyprodaný pouze v případě, že nejsou skladem všechny jeho varianty.

Po dokončení všech předchozích konfiguračních kroků zobrazí zpřesňující parametry na stránkách s výsledky vyhledávání filtr založený na inventáři a modul výsledků vyhledávání načte data inventáře ze zákulisí. Poté můžete nakonfigurovat **Nastavení zásob pro stránky se seznamem produktů** v nástroji Commerce Site Builder, abyste mohli ovládat, jak modul výsledků vyhledávání zobrazuje produkty, které nejsou skladem. Další informace [Použít nastavení zásob](inventory-settings.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul rychlého zobrazení](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
