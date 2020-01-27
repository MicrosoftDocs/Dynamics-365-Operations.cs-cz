---
title: Integrace Power Apps
description: Toto téma popisuje způsob vložení Power Apps do klienta pro zvýšení funkčnosti produktu.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870234"
---
# <a name="embed-microsoft-power-apps"></a>Integrace Microsoft Power Apps

[!include [banner](../includes/banner.md)]

AktualizacE Platform Update 14 podporuje integraci s Microsoft Power Apps, službou pro vývojáře a netechnické uživatele pro vytváření vlastních obchodních aplikací pro mobilní zařízení, tablety a web bez zápisu kódu. Power Apps, které jste vytvořili vy, vaše organizace nebo širší ekosystém, lze poté vložit do aplikací Finance and Operations, aby bylo možné vylepšit funkce produktu. Například může vytvořit PowerApp pro doplnění aplikací Finance and Operations informacemi získanými z jiného systému.

Další informace o začlenění Power Apps se dozvíte v krátkém videu [Jak začlenit PowerApps do Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Přidání vložené PowerApp na stránku

### <a name="overview"></a>Přehled

Před vložením PowerApp do klienta je nejdříve nutné najít nebo vytvořit PowerApp s požadovanými vizuály nebo funkcemi. Nepopíšeme zde podrobný proces vytváření PowerApp. Téma [Úvod do Power Apps](https://docs.microsoft.com/powerapps/getting-started) je ideálním výchozím bodem, pokud s Power Apps začínáte.

Až budete připraveni integrovat konkrétní PowerApp, můžete si vybrat mezi dvěma způsoby přístupu k PowerApp na stránce, podle toho, který postup lépe vyhovuje vašim potřebám. První způsob je pomocí tlačítka Power Apps, které bylo přidáno do standardního podokna akcí. Power Apps přidané pomocí tohoto mechanismu se budou zobrazovat jako položky nabídky uvnitř tlačítka nabídky Power Apps. Jsou-li vybrané, otevřou všechny tyto položky nabídky podokno obsahující vloženou PowerApp. Alternativně se můžete rozhodnout rovněž zobrazit PowerApp přímo na stránce jako novou kartu, pevnou záložku, list nebo nový oddíl v pracovním prostoru.

Při konfiguraci vaší integrované PowerApp můžete vybrat jednoho pole, které má být odesláno jako vstup do PowerApp. To umožňuje, aby PowerApp reagovala na základě dat, které se aktuálně zobrazují.

### <a name="details"></a>Podrobnosti

Následující pokyny popisují postup integrace PowerApp do webového klienta.

1. Přejděte na stránku, kam chcete vložit PowerApp. Bude se jednat o stejnou stránku, která obsahuje všechna data potřebná k předání do PowerApp jako vstup.
2. Otevřete podokno **Vložit PowerApp**:

    - Klepněte na tlačítko **možnosti** a poté vyberte **přizpůsobit tento formulář**. V nabídce **Vložit** zvolte **PowerApp**. Nakonec vyberte oblast, kam chcete přidat PowerApp. Pokud se má vložit PowerApp pod tlačítkem nabídky Power Apps, vyberte podokno akcí. Pokud se má vložit PowerApp přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru).
    - Pokud bude do PowerApp získán přístup pomocí tlačítka nabídky Power Apps, můžete rovněž klepnout na tlačítko nabídky **Power Apps** v podokně akcí a poté vybrat vložit **vložit PowerApp**.

3. Konfigurace vložené PowerApp:

    - Pole **Název** označuje text zobrazený pro tlačítko nebo kartu, které budou obsahovat integrovanou PowerApp. Často můžete chtít opakovat název PowerApp v tomto poli.
    - **ID aplikace** je identifikátor GUID pro PowerApp, který má být vložen. Chcete-li načíst tuto hodnotu, vyhledejte PowerApp na [web.powerapps.com](https://web.powerapps.com) a vyhledejte pole **ID aplikace** pod položkou **Podrobnosti**.
    - Pro **vstupní data pro PowerApp** lze volitelně vybrat pole obsahující data, která je nutné předat do PowerApp jako vstup. Podrobné informace o přístupu PowerApp k datům odeslaným z aplikací Finance and Operations naleznete v části tohoto tématu nazvané [Vytvoření PowerApp, která využívá data z aplikací Finance and Operations](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Zvolte **velikost aplikace** odpovídající typu PowerApp, který vkládáte. Vyberte **Tenký** pro aplikace Power Apps vytvořené pro mobilní zařízení a **Široký** pro Power Apps vytvořené pro tablety. To zajišťuje, že je pro integrovanou PowerApp vyhrazeno dostatečné množství místa.
    - Pevná záložka **Právnické osoby** poskytuje možnost zvolit, pro jaké právnické osoby je PowerApp dostupná. Výchozí nastavení je pro zobrazení PowerApp ve všech právnických osobách.

4. Po potvrzení správnosti konfigurace klepněte na tlačítko **Vložit** pro vložení PowerApp na stránku. Budete vyzváni k obnovení prohlížeče, aby se zobrazila integrovaná PowerApp.

## <a name="sharing-an-embedded-power-app"></a>Sdílení integrované PowerApp

Po vložení PowerApp na stránku a ověření, že pracuje správně v jakémkoli kontextu dat předaném ze stránky můžete sdílet tuto vloženou PowerApp s ostatními uživateli v systému. Toho lze dosáhnout dvěma různými způsoby pomocí možností individuálního nastavení produktu:

- Doporučený scénář je prostřednictvím správce systému, který může individuální nastavení předat všem uživatelům nebo podmnožině uživatelů.
- Případně můžete exportovat přizpůsobení své stránky, zaslat je jednomu nebo více uživatelům a nechat tyto jednotlivé uživatelé importovat vaše změny. Možnost Spravovat na panelu nástrojů induviduálního nastavení vám umožní exportovat a importovat individuální nastavení.

Podrobnější informace o možnostech přizpůsobení v produktu a jejich použití naleznete v tématu [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Vytváření PowerApp, která využívá data odeslaná z aplikací Finance and Operations

Důležitou část vytváření PowerApp, které budou vloženy do aplikací Finance and Operations je používání vstupních dat z aplikací Finance and Operations. Uvnitř PowerApp lze k těmto vstupním datům získat přístup proměnné Param("EntityId").

Například ve funkci Při spuštění PowerApp můžete nastavit vstupní data z aplikací Finance and Operations následujícím způsobem:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Zobrazení integrované PowerApp

Chcete-li zobrazit integrovanou PowerApp na stránce v aplikacích Finance and Operations, jednoduše přejděte na stránku s integrovanou PowerApp. Vzpomeňte si. že k Power Apps lze přistupovat prostřednictvím tlačítka Power Apps ve standardním podokně akcí, nebo se mohou zobrazit přímo na stránce jako nová karta, pevná záložka nebo jako nová část v pracovním prostoru. Když se uživatel pokusí načíst PowerApp na stránce poprvé, bude vyzván k přihlášení do Power Apps, aby se zajistilo, že má příslušná oprávnění k použití PowerApp.

## <a name="editing-an-embedded-power-app"></a>Úprava integrované PowerApp

Poté, co byla vložena PowerApp na stránku, je nutné provést změny v konfiguraci této PowerApp. Možná například chcete změnit popisek přidružené vložené PowerApp nebo byla vytvořena nová verze PowerApp a je nutné aktualizovat na poslední ID aplikace odkazující na PowerApp.

Následovně můžete upravit konfiguraci vložených PowerApp:

1. Přejděte do podokna **Upravit PowerApp**.

    - Je-li vložená PowerApp otevírána přes tlačítko nabídky Power Apps, klikněte pravým tlačítkem myši na tlačítko Power Apps a vyberte **Přizpůsobit** Vyberte PowerApp, kterou chcete konfigurovat z rozevírací nabídky **Zvolit PowerApp**.
    - Pokud se vložená PowerApp zobrazí přímo na stránce, vyberte **Možnosti** a potom **Přizpůsobit tento formulář**. S použitím nástroje **Vybrat** klikněte na integrovanou PowerApp.

2. Proveďte potřebné změny konfigurace Power Apps a klepněte na tlačítko **Uložit**.

## <a name="removing-an-embedded-power-app"></a>Odstranění integrované PowerApp

Poté, co byla vložena PowerApp na stránku, existují dva způsoby, jak ji odebrat v případě potřeby:

- Přejděte do podokna **Upravit PowerApp** podle pokynů v části [Úpravy vložené PowerApp](#editing-an-embedded-power-app) dříve v tomto tématu. Potvrďte, že se v podokně zobrazí informace o vložené PowerApp, kterou chcete odebrat, a klepněte na tlačítko **odstranit**.
- Vzhledem k tomu, že vložená PowerApp je uložena jako údaj o individuálním nastavení, clearing přizpůsobení stránky rovněž odstraní všechny Power Apps vložené na této stránce. Poznámka: zrušení zaškrtnutí přizpůsobení stránky je trvalé a nelze je vrátit zpět. Chcete-li odebrat vaše individuální nastavení na stránce, vyberte **Možnosti** a klikněte na **Přizpůsobit tento formulář**. V nabídce **Spravovat** zvolte tlačítko **Vymazat**. Po aktualizaci prohlížeče budou odebrána všechna předchozí individuální nastavení pro tuto stránku. Další informace o optimalizaci stránek pomocí individuálního nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="appendix"></a>Dodatek

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Vývojář může kontrolovat, kam lze PowerApp vložit.

Podle výchozího nastavení uživatel může vložit Power Apps na každou stránku pod tlačítkem nabídky Power Apps nebo přímo na stránku jako kartu, pevnou záložku, list nebo jako nový oddíl v pracovním prostoru. Avšak v případě potřeby vývojáři také mohou konfigurovat tuto funkci, aby povolila vnoření Power Apps pouze na některé stránky pomocí následujících metod:

- **isPowerAppPersonalizationEnabled** – Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, pak tlačítko nabídky Power Apps nebude zobrazeno a uživatelé nebudou moci vkládat Power Apps kamkoli na tuto stránku, včetně karty.
- **isPowerAppTabPersonalizationEnabled** – Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, potom uživatelé nebudou moci vkládat Power Apps přímo na stránku jako kartu, pevnou záložku nebo oddíl panoramatu. Uživatelé budou moci vložit Power Apps pomocí tlačítka nabídky Power Apps je-li vkládání na stránce povoleno.

Následující příklad ukazuje novou třídu s dvěma metodami potřebnými ke konfigurace, kde má být Power Apps vložena.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
