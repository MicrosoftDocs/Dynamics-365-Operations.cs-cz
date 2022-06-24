---
title: Vložení aplikací plátna z Power Apps
description: Tento článek popisuje způsob vložení aplikací plátna z Microsoft Power Apps do klienta pro zvýšení funkčnosti produktu.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fb81aa058e749df346ee87bbe83427b20b234b72
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898391"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Vložit aplikace plátna z Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps je službou umožňující vývojářům i netechnickým uživatelům vytvářet vlastní obchodní aplikace pro mobilní zařízení, tablety a web bez psaní kódu. Finanční a provozní aplikace podporují integraci s Power Apps. Aplikace plátna, které jste vytvořili vy, vaše organizace nebo širší ekosystém, lze vložit do finančních a provozních aplikací, aby bylo možné vylepšit funkce produktu. Například můžete vytvořit aplikaci plátna z Power Apps pro doplnění finanční a provozní aplikace o informace získané z jiného systému.

Další informace o začlenění aplikací plátna se dozvíte v krátkém videu [Jak začlenit aplikace plátna](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Přidání vložené aplikace plátna Power Apps na stránku

Před vložením aplikace plátna z Power Apps do klienta je nejdříve nutné najít nebo vytvořit aplikaci s požadovanými vizuály nebo funkcemi. Tento článek neobsahuje podrobný popis procesu vytváření aplikací. Pokud jsou pro vás Power Apps novinkou, přečtěte si [dokumentaci Power Apps](/powerapps/).

Existují tři způsoby, jak vložit aplikaci plátna do finanční a provozní aplikace. Můžete použít přístup, který nejlépe odpovídá vašemu scénáři. 

- Vložte aplikaci plátna do tlačítka **Power Apps** ve standardním podokně akcí stránky. Aplikace, které přidáte tímto způsobem, se zobrazí jako položky na tlačítku nabídky **Power Apps** a aplikace se otevírají v bočních podoknech. 
- Vložte aplikaci plátna na existující stránku jako stránku nové karty (kontingenční karta, rychlá karta, okno nebo část pracovního prostoru).
- Vytvořte na řídicím panelu nové celostránkové prostředí pro aplikaci plátna.

Při konfiguraci vaší integrované aplikace plátna můžete vybrat jednoho pole, které má být odesláno jako kontext do aplikace. Tento krok umožňuje, aby aplikace reagovala na základě dat, které se aktuálně zobrazují.

> [!NOTE]
> Tento mechanismus nemůžete použít k vložení modelem řízených aplikací.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Vložení aplikace plátna na existující stránku

Následující postup ukazuje, jak vložit aplikaci plátna z Power Apps na existující stránku.

1. Přejděte na stránku, kam chcete vložit aplikaci plátna. Tato stránka bude obsahovat všechna data nutná k předání do aplikace jako vstup.
2. Otevřete podokno **Přidat aplikaci z Power Apps**:

    - Pokud bude aplikace vložena přímo na stránku, vyberte **Možnosti** \> **Personalizujte tuto stránku** \> **Další** a poté proveďte jeden z těchto kroků:

        - Pokud je zapnuta funkce **Celostránkové aplikace**, vyberte **Přidat stránku** a poté vyberte oblast, kam chcete aplikaci přidat. Chcete-li aplikaci vložit do tlačítka nabídky **Power Apps**, vyberte podokno akcí. Chcete-li vložit aplikace přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru). Poté v podokně **Přidat aplikaci** vyberte **Power Apps**.
        - Pokud je vypnuta funkce **Celostránkové aplikace**, vyberte **Přidat aplikaci z Power Apps** a poté vyberte oblast, kam chcete aplikaci přidat. Chcete-li aplikaci vložit do tlačítka nabídky **Power Apps**, vyberte podokno akcí. Chcete-li vložit aplikace přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru).

    - Pokud bude do aplikace získán přístup pomocí tlačítka nabídky **Power Apps**, můžete vybrat tlačítko nabídky **Power Apps** v podokně akcí a poté vybrat **Přidat aplikaci**.

3. Konfigurace vložené aplikace. Více informací naleznete v části [Konfigurace aplikace plátna](#configuring-a-canvas-app) v dále v tomto článku.
4. Poté, co potvrdíte, že je konfigurace správná, vyberte **Vložit**.

    - Pokud je funkce **Uložená zobrazení** vypnutá, budete vyzváni k obnovení prohlížeče, aby se zobrazila vložená aplikace.
    - Pokud je funkce **Uložená zobrazení** zapnutá, musíte zobrazení uložit, aby změna trvala.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Vložení apliace plátna jako celostránkového prostředí z řídicího panelu

Možná chcete vložit aplikaci plátna z řídicího panelu, pokud aplikace nesouvisí s existující stránkou nebo pokud pouze chcete, aby byla aplikace celostránkovým prostředím uvnitř finanční a provozní aplikace.

> [!NOTE]
> Chcete-li tuto možnost zpřístupnit, musíte zapnout funkci **Celostránkové aplikace** ve správě funkcí. 

1. Otevřete řídicí panel.
2. Vyberte a podržte (nebo klikněte pravým tlačítkem) stránku, vyberte **Přizpůsobit** a potom vyberte **Přidat stránku**.
3. V podokně **Přidat stránku** Vyberte **Power Apps**.
4. Konfigurace vložené aplikace. Více informací naleznete v části [Konfigurace aplikace plátna](#configuring-a-canvas-app) v dále v tomto článku.
5. Vyberte **Uložit** pro přidání aplikace na řídicí panel jako nové dlaždice.
6. Vyberte novou dlaždici na řídicím panelu a potvrďte, že se aplikace plátna zobrazí podle očekávání.

### <a name="configuring-a-canvas-app"></a>Konfigurace aplikace plátna

Když vložíte aplikaci plátna, musíte nastavit následující parametry:

- **Název** – Zadejte text, který by se měl zobrazit pro tlačítko nebo kartu, která bude obsahovat vloženou aplikaci. Často můžete chtít opakovat název aplikace v tomto poli.
- **ID aplikace** - označuje globálně jedinečný identifikátor (GUID) pro aplikaci plátna, kterou chcete vložit. Chcete-li načíst tuto hodnotu, vyhledejte aplikaci na webu [make.powerapps.com](https://make.powerapps.com) a pak se podívejte do pole **ID aplikace** pod položkou **Podrobnosti**.
- **Vstupní kontext pro aplikaci** - můžete volitelně vybrat pole obsahující data, která je nutné předat do aplikace jako vstup. Informace o přístupu aplikace k datům odeslaným z finančních a provozních aplikací naleznete v části tohoto článku nazvané [Vytvoření aplikace, která využívá data z finančních a provozních aplikací](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps).

    Počínaje verzí 10.0.19 je aktuální právnická osoba také předána jako kontext do aplikace plátna prostřednictvím parametru URL **cmp**. Toto chování neovlivní cílovou aplikaci plátna, dokud tato aplikace tyto informace nepoužije.

- **Velikost aplikace** - vyberte typ aplikace, kterou vkládáte. Vyberte **Tenký** pro aplikace vytvořené pro mobilní zařízení nebo **Široký** pro aplikace vytvořené pro tablety. Tento parametr zajišťuje, že je pro vloženou aplikaci vyhrazeno dostatečné množství místa.
- **Právnické osoby** - Můžete vybrat právnické osoby, pro které by měla být aplikace k dispozici. Ve výchozím nastavení je aplikace k dispozici pro všechny právnické osoby. Tato možnost je k dispozici pouze v případě, že vložíte přímo na existující stránku a funkce **[Uložená zobrazení](saved-views.md)** je vypnutá.

## <a name="sharing-an-embedded-app"></a>Sdílení integrované aplikace

Po vložení aplikace plátna na stránku a ověření, že pracuje správně, můžete sdílet tuto vloženou aplikaci s ostatními uživateli v systému. Chcete-li sdílet vloženou aplikaci plátna, postupujte takto.

1. [Sdílejte aplikaci plátna v Power Apps](/powerapps/maker/canvas-apps/share-app) s příslušnými uživateli, aby měli přístup k aplikaci přímo v Power Apps.
2. Sdílejte personalizace, které jsou přidružené k integrované aplikaci, s požadovanými uživateli. Můžete použít některý z následujících způsobů.

    - **Publikovat zobrazení (doporučeno):** Pokud je funkce **[Uložená zobrazení](saved-views.md)** zapnutá, doporučeným a upřednostňovaným přístupem je vytvořit zobrazení, které obsahuje vloženou aplikaci plátna, a poté toto zobrazení publikovat požadovaným uživatelům. Tento způsob zajišťuje, že aplikaci plátna na stránce uvidí všichni uživatelé, kteří mají role zabezpečení, na které se cílí publikované zobrazení.

        Z řídicího panelu můžete také publikovat aplikaci plátna, která byla vložena jako celostránkové prostředí. Na řídicím panelu vyberte a podržte (nebo klikněte pravým tlačítkem) dlaždici přidruženou k aplikaci, vyberte **Přizpůsobit** a potom vyberte **Publikovat stránku**. Prostředí, které se podobá prostředí *Zobrazení publikování* je zobrazeno a můžete vybrat role zabezpečení, do kterých chcete publikovat. V aktualizaci 10.0.21 nebo novější, pokud je funkce **Vylepšená podpora právnických osob pro uložená zobrazení** zapnutá, můžete aplikaci také publikovat na požadované právnické osoby.

    - Pokud je funkce **Uložená zobrazení** vypnutá, správce systému může poskytnout přizpůsobení, které zahrnuje aplikaci plátna, příslušné sadě uživatelů prostřednictvím stránky **Personalizace**. Případně můžete exportovat přizpůsobení své stránky a odeslat je jednomu nebo více uživatelům. Každý z těchto uživatelů pak může importovat personalizace. Panel nástrojů individuálního nastavení obsahuje tlačítka, které vám umožní exportovat a importovat individuální nastavení.

> [!NOTE]
> Pokud byla aplikace plátna sdílena s externími uživateli, nemohou tito uživatelé použít vloženou aplikaci uvnitř finanční a provozní aplikace. Mohou však přistupovat k aplikaci přímo uvnitř Power Apps. Externí uživatelé zahrnují hosty a uživatele, kteří nepatří do Microsoft 365 Azure Directory, kde je finanční a provozní aplikace nasazena.

Podrobnější informace o možnostech přizpůsobení v produktu a jejich použití naleznete v tématu [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Vytváření aplikace plátna, která používá data odesílaná z finančních a provozních aplikací

Když vytvoříte aplikaci plátna, která bude vložena do finanční a provozní aplikace, jednou důležitou součástí procesu je použití vstupních dat z této finanční a provozní aplikace. Z vývojového prostředí Power Apps lze vstupní data předaná z finanční a provozní aplikace otevřít pomocí proměnné **Param("EntityId")**. Díle počínaje verzí 10.0.19 bude aktuální právnická osoba také předána do aplikace plátna prostřednictvím proměnné **Param("cmp")**. 

Například ve funkci Při spuštění aplikace můžete nastavit vstupní data z finančních a provozních aplikací následujícím způsobem:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Prohlížení aplikace plátna

Chcete-li zobrazit vloženou aplikaci plátna na stránce v finančních a provozních aplikacích, jednoduše přejděte na stránku s vloženou aplikací. Nezapomeňte, že k aplikacím lze přistupovat pomocí tlačítka **Power Apps** ve standardním podokně akcí. Alternativně se mohou objevit přímo na stránce jako nová karta, záložku s náhledem, okno nebo nový oddíl v pracovním prostoru. Když se uživatelé poprvé pokusí načíst aplikaci na stránku, budou vyzváni k přihlášení. Tento krok zajišťuje, že uživatelé mají příslušná oprávnění k používání aplikace.

## <a name="editing-an-embedded-app"></a>Úprava integrované aplikace

Poté, co byla vložena aplikace na stránku, je nutné provést změny v konfiguraci této aplikace. Možná například chcete změnit popisek přidružené vložené aplikace nebo byla vytvořena nová verze aplikace a je nutné aktualizovat na poslední ID aplikace odkazující na aplikaci.

Následovně můžete upravit konfiguraci vložených aplikací:

1. Přejděte do podokna **Upravit aplikaci**.

    - Je-li vložená aplikace otevírána přes tlačítko nabídky Power Apps, vyberte a podržte (případně klikněte pravým tlačítkem myši) tlačítko Power Apps a vyberte **Přizpůsobit**. Vyberte aplikaci, kterou chcete konfigurovat z rozevírací nabídky **Zvolit aplikaci**.
    - Pokud se vložená aplikace zobrazí přímo na stránce, vyberte **Možnosti** a potom **Přizpůsobit tuto stránku**. S použitím nástroje **Vybrat** klikněte na integrovanou aplikaci.
    - Pokud byla integrovaná aplikace přidána z řídicího panelu, otevřete řídicí panel, vyberte a podržte (nebo klikněte pravým tlačítkem) dlaždici, která je přidružena k aplikaci plátna, vyberte **Přizpůsobit** a poté vyberte **Upravit stránku**.

2. Proveďte potřebné změny konfigurace aplikace a klikněte na tlačítko **Uložit**.

## <a name="removing-an-app"></a>Odebírání aplikace

Poté, co byla vložena aplikace na stránku, existuje několik způsobů, jak ji odebrat v případě potřeby:

- Přejděte do podokna **Upravit aplikaci** podle pokynů v části [Úpravy vložené aplikace](#editing-an-embedded-app) dříve v tomto článku. Potvrďte, že se v podokně zobrazí informace o vložené aplikaci, kterou chcete odebrat, a klepněte na tlačítko **Odstranit**.
- Pokud byla integrovaná aplikace přidána z řídicího panelu, otevřete řídicí panel, vyberte a podržte (nebo klikněte pravým tlačítkem) dlaždici, která je přidružena k aplikaci plátna, vyberte **Přizpůsobit** a poté vyberte **Odebrat stránku**. 
- Vzhledem k tomu, že vložená aplikace je uložena jako údaj o individuálním nastavení, clearing přizpůsobení stránky rovněž odstraní všechny aplikace vložené na této stránce. Poznámka: zrušení zaškrtnutí přizpůsobení stránky je trvalé a nelze je vrátit zpět. Chcete-li odebrat vaše individuální nastavení na stránce, vyberte **Možnosti** a klikněte na **Přizpůsobit tuto stránku** a nakonec na **Vymazat**. Po aktualizaci prohlížeče budou odebrána všechna předchozí individuální nastavení pro tuto stránku. Další informace o optimalizaci stránek pomocí individuálního nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="appendix"></a>Dodatek

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Vývojář] Modelování aplikace plátna na formuláři

I když se tento článek zaměřuje na vkládání aplikací plátna pomocí personalizace, vývojáři mají také možnost přidat aplikaci plátna do formuláře pomocí vývojářského prostředí Visual Studio. Chcete-li to provést, jednoduše do formuláře přidejte PowerAppsHostControl. Vlastnosti metadat, které jsou k dispozici pro ovládací prvek, poskytují stejné možnosti jako prostředí přizpůsobení.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Vývojář] specifikuje, kam lze aplikaci vložit.

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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
