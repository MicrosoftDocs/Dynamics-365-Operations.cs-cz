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
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042935"
---
# <a name="embed-microsoft-power-apps"></a>Integrace Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations podporuje integraci s Microsoft Power Apps, službou pro vývojáře a netechnické uživatele pro vytváření vlastních obchodních aplikací pro mobilní zařízení, tablety a web bez zápisu kódu. Power Apps, které jste vytvořili vy, vaše organizace nebo širší ekosystém, lze poté vložit do aplikací Finance and Operations, aby bylo možné vylepšit funkce produktu. Například může vytvořit aplikaci z Power Apps pro doplněí aplikace Finance and Operations s informacemi získanými z jiného systému.

Další informace o začlenění Power Apps se dozvíte v krátkém videu [Jak začlenit PowerApps do Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Přidání vložené aplikace Power Apps na stránku

### <a name="overview"></a>Přehled

Před vložením aplikace z Power Apps do klienta je nejdříve nutné najít nebo vytvořit aplikaci s požadovanými vizuály nebo funkcemi. Nepopíšeme zde podrobný proces vytváření aplikací. Téma [Úvod do Power Apps](https://docs.microsoft.com/powerapps/getting-started) je ideálním výchozím bodem, pokud s Power Apps začínáte.

Až budete připraveni integrovat konkrétní aplikaci, můžete si vybrat mezi dvěma způsoby přístupu k aplikaci na stránce, podle toho, který postup lépe vyhovuje vašim potřebám. První způsob je pomocí tlačítka Power Apps, které bylo přidáno do standardního podokna akcí. Aplikace přidané pomocí tohoto mechanismu se budou zobrazovat jako položky nabídky uvnitř tlačítka nabídky Power Apps. Jsou-li vybrané, otevřou všechny tyto položky nabídky podokno obsahující vloženou aplikaci. Alternativně se můžete rozhodnout vložit aplikaci přímo na stránce jako novou kartu, záložku s náhledem, list nebo nový oddíl v pracovním prostoru.

Při konfiguraci vaší integrované aplikace můžete vybrat jednoho pole, které má být odesláno jako kontext do aplikace. To umožňuje, aby aplikace reagovala na základě dat, které se aktuálně zobrazují.

### <a name="details"></a>Podrobnosti

Následující pokyny popisují postup integrace aplikace z Power Apps do webového klienta.

1. Přejděte na stránku, kam chcete vložit aplikaci. Bude se jednat o stejnou stránku, která obsahuje všechna data potřebná k předání do aplikace jako vstup.
2. Otevřete podokno **Přidat aplikaci z Power Apps**:

    - Klepněte na tlačítko **možnosti** a poté vyberte **Přizpůsobit tuto stránku**. V nabídce **Vložit** zvolte **Power Apps**. Nakonec vyberte oblast, kam chcete přidat aplikaci. Pokud se má vložit aplikace pod tlačítkem nabídky Power Apps, vyberte podokno akcí. Pokud se má vložit aplikace přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru).
    - Pokud bude do aplikace získán přístup pomocí tlačítka nabídky Power Apps, můžete rovněž kliknout na tlačítko nabídky **Power Apps** v podokně akcí a poté vybrat **Přidat aplikaci**.

3. Konfigurace vložené aplikace:

    - Pole **Název** označuje text zobrazený pro tlačítko nebo kartu, které budou obsahovat integrovanou aplikaci. Často můžete chtít opakovat název aplikace v tomto poli.
    - **ID aplikace** je identifikátor GUID pro aplikaci, která má být vložena. Chcete-li načíst tuto hodnotu, vyhledejte aplikaci na [web.powerapps.com](https://web.powerapps.com) a vyhledejte pole **ID aplikace** pod položkou **Podrobnosti**.
    - Pro **Vstupní kontext pro aplikaci** lze volitelně vybrat pole obsahující data, která je nutné předat do aplikace jako vstup. Dále v pozdější části tohoto tématu [Vytvoření aplikace, která využívá data odeslaná z aplikací Finance and Operations](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps) získáte podrobné informace o přístupu aplikace k datům odeslaným z aplikací Finance and Operations.
    - Zvolte **velikost aplikace** odpovídající typu aplikace, kterou vkládáte. Vyberte **Tenký** pro aplikace vytvořené pro mobilní zařízení a **Široký** pro aplikace vytvořené pro tablety. To zajišťuje, že je pro integrovanou aplikaci vyhrazeno dostatečné množství místa.
    - Pevná záložka **Právnické osoby** poskytuje možnost zvolit, pro jaké právnické osoby je aplikace dostupná. Výchozí nastavení je učinit aplikaci přístupnou všem právnickým osobám. Tato možnost je k dispozici pouze tehdy, je-li zakázána funkce [uložená zobrazení](saved-views.md). 

4. Po potvrzení správnosti konfigurace klepněte na tlačítko **Vložit** pro vložení PowerApp na stránku. Budete vyzváni k obnovení prohlížeče, aby se zobrazila integrovaná aplikace.

## <a name="sharing-an-embedded-app"></a>Sdílení integrované aplikace

Po vložení aplikace na stránku a ověření, že pracuje správně v jakémkoli kontextu dat předaném ze stránky můžete sdílet tuto vloženou aplikaci s ostatními uživateli v systému. Toho lze dosáhnout dvěma různými způsoby pomocí možností individuálního nastavení produktu:

- Doporučený scénář je prostřednictvím správce systému, který může individuální nastavení předat všem uživatelům nebo podmnožině uživatelů.
- Případně můžete exportovat přizpůsobení své stránky, zaslat je jednomu nebo více uživatelům a nechat tyto jednotlivé uživatelé importovat vaše změny. Panel nástrojů individuálního nastavení obsahuje akce, které vám umožní exportovat a importovat individuální nastavení.

Podrobnější informace o možnostech přizpůsobení v produktu a jejich použití naleznete v tématu [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Vytváření aplikace, která využívá data odesílaná z aplikací Finance and Operations

Důležitou součástí vytváření aplikace z Power Apps, které jsou vloženy do aplikace Finance and Operations, je využití vstupních dat z této aplikace. Z vývojového prostředí Power Apps lze vstupní data předaná z Finance and Operations otevřít pomocí proměnné Param("EntityId").

Například ve funkci Při spuštění aplikace můžete nastavit vstupní data z aplikací Finance and Operations do proměnné následujícím způsobem:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Zobrazení aplikace

Chcete-li zobrazit integrovanou aplikaci na stránce v aplikacích Finance and Operations, jednoduše přejděte na stránku s integrovanou aplikací. Vzpomeňte si. že k aplikacím lze přistupovat prostřednictvím tlačítka Power Apps ve standardním podokně akcí, nebo se mohou zobrazit přímo na stránce jako nová karta, pevná záložka nebo jako nová část v pracovním prostoru. Když se uživatel pokusí načíst aplikaci na stránce poprvé, bude vyzván k přihlášení do , aby se zajistilo, že má příslušná oprávnění k použití aplikace.

## <a name="editing-an-embedded-app"></a>Úprava integrované aplikace

Poté, co byla vložena aplikace na stránku, je nutné provést změny v konfiguraci této aplikace. Možná například chcete změnit popisek přidružené vložené aplikace nebo byla vytvořena nová verze aplikace a je nutné aktualizovat na poslední ID aplikace odkazující na aplikaci.

Následovně můžete upravit konfiguraci vložených aplikací:

1. Přejděte do podokna **Upravit aplikaci**.

    - Je-li vložená aplikace otevírána přes tlačítko nabídky Power Apps, klikněte pravým tlačítkem myši na tlačítko Power Apps a vyberte **Přizpůsobit**. Vyberte aplikaci, kterou chcete konfigurovat z rozevírací nabídky **Zvolit aplikaci**.
    - Pokud se vložená aplikace zobrazí přímo na stránce, vyberte **Možnosti** a potom **Přizpůsobit tuto stránku**. S použitím nástroje **Vybrat** klikněte na integrovanou aplikaci.

2. Proveďte potřebné změny konfigurace aplikace a klikněte na tlačítko **Uložit**.

## <a name="removing-an-app"></a>Odebírání aplikace

Poté, co byla vložena aplikace na stránku, existují dva způsoby, jak ji odebrat v případě potřeby:

- Přejděte do podokna **Upravit aplikaci** podle pokynů v části [Úpravy vložené aplikace](#editing-an-embedded-app) dříve v tomto tématu. Potvrďte, že se v podokně zobrazí informace o vložené aplikaci, kterou chcete odebrat, a klepněte na tlačítko **Odstranit**.
- Vzhledem k tomu, že vložená aplikace je uložena jako údaj o individuálním nastavení, clearing přizpůsobení stránky rovněž odstraní všechny aplikace vložené na této stránce. Poznámka: zrušení zaškrtnutí přizpůsobení stránky je trvalé a nelze je vrátit zpět. Chcete-li odebrat vaše individuální nastavení na stránce, vyberte **Možnosti** a klikněte na **Přizpůsobit tuto stránku** a nakonec na **Vymazat**. Po aktualizaci prohlížeče budou odebrána všechna předchozí individuální nastavení pro tuto stránku. Další informace o optimalizaci stránek pomocí individuálního nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="appendix"></a>Dodatek

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Vývojář může kontrolovat, kam lze aplikaci vložit.

Podle výchozího nastavení uživatel může vložit aplikace na každou stránku pod tlačítkem nabídky Power Apps nebo přímo na stránku jako kartu, pevnou záložku, list nebo jako nový oddíl v pracovním prostoru. Avšak v případě potřeby vývojáři také mohou konfigurovat tuto funkci, aby povolila vložení aplikace pouze na některé stránky pomocí následujících metod:

- **isPowerAppPersonalizationEnabled** – Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, pak tlačítko nabídky Power Apps nebude zobrazeno a uživatelé nebudou moci vkládat aplikace kamkoli na tuto stránku, včetně karty.
- **isPowerAppTabPersonalizationEnabled** -- Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, potom uživatelé nebudou moci vkládat aplikace přímo na stránku jako kartu, pevnou záložku nebo oddíl panoramatu. Uživatelé budou moci vložit aplikace pomocí tlačítka nabídky Power Apps, je-li vkládání na stránce povoleno.

Následující příklad ukazuje novou třídu s dvěma metodami potřebnými ke konfigurace, kde mají být aplikace vloženy.

```powerapps
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
