---
title: Vložit aplikace plátna z Power Apps
description: Toto téma popisuje způsob vložení aplikací plátna z Microsoft Power Apps do klienta pro zvýšení funkčnosti produktu.
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
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
ms.openlocfilehash: f8c7ad4322de594a06a09102c8eb7d09299d1d71
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564777"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Vložit aplikace plátna z Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps je službou umožňující vývojářům i netechnickým uživatelům vytvářet vlastní obchodní aplikace pro mobilní zařízení, tablety a web bez psaní kódu. Aplikace Finance and Operations podporují integraci s Power Apps. Aplikace plátna, které jste vytvořili vy, vaše organizace nebo širší ekosystém, lze vložit do aplikací Finance and Operations, aby bylo možné vylepšit funkce produktu. Například můžete vytvořit aplikaci plátna z Power Apps pro doplnění aplikace Finance and Operations o informace získané z jiného systému.

Další informace o začlenění Power Apps se dozvíte v krátkém videu [Jak začlenit PowerApps do Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Přidání vložené aplikace plátna Power Apps na stránku

### <a name="overview"></a>Přehled

Před vložením aplikace plátna z Power Apps do klienta je nejdříve nutné najít nebo vytvořit aplikaci s požadovanými vizuály nebo funkcemi. Toto téma neobsahuje podrobný popis procesu vytváření aplikací. Pokud jsou pro vás Power Apps novinkou, přečtěte si [dokumentaci Power Apps](https://docs.microsoft.com/powerapps/).

Když jste připraveni aplikaci vložit, můžete se ke konkrétní aplikaci plátna na stránce dostat dvěma způsoby. Můžete si vybrat, který přístup lépe vyhovuje vašemu scénáři. První způsob je pomocí tlačítka **Power Apps**, které bylo přidáno do standardního podokna akcí. Aplikace, které přidáte pomocí tohoto postupu, se zobrazí jako položky na tlačítku nabídky **Power Apps**. Když vyberte jednu z těchto položek, objeví se postranní podokno obsahující vloženou aplikaci. Alternativně můžete vložit aplikaci přímo na stránce jako novou kartu, záložku s náhledem, list nebo nový oddíl v pracovním prostoru.

Při konfiguraci vaší integrované aplikace plátna můžete vybrat jednoho pole, které má být odesláno jako kontext do aplikace. Tento krok umožňuje, aby aplikace reagovala na základě dat, které se aktuálně zobrazují.

> [!NOTE]
> Tento mechanismus aktuálně nemůžete použít k vložení modelovaných aplikací.  

### <a name="details"></a>Podrobnosti

Následující postup ukazuje, jak vložit aplikaci plátna z Power Apps do webového klienta.

1. Přejděte na stránku, kam chcete vložit aplikaci plátna. Bude se jednat o stránku, která obsahuje všechna data nutná k předání do aplikace jako vstup.
2. Otevřete podokno **Přidat aplikaci z Power Apps**:

    - Klepněte na tlačítko **možnosti** a poté vyberte **Přizpůsobit tuto stránku**. V nabídce **Vložit** zvolte **Power Apps**. Nakonec vyberte oblast, kam chcete přidat aplikaci. Pokud se má vložit aplikace pod tlačítkem nabídky Power Apps, vyberte podokno akcí. Pokud se má vložit aplikace přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru).
    - Pokud bude do aplikace získán přístup pomocí tlačítka nabídky Power Apps, můžete rovněž kliknout na tlačítko nabídky **Power Apps** v podokně akcí a poté vybrat **Přidat aplikaci**.

3. Konfigurace vložené aplikace:

    - Pole **Název** označuje text zobrazený pro tlačítko nebo kartu, které budou obsahovat integrovanou aplikaci. Často můžete chtít opakovat název aplikace v tomto poli.
    - Pole **ID aplikace** označuje globálně jedinečný identifikátor (GUID) pro aplikaci plátna, kterou chcete vložit. Chcete-li načíst tuto hodnotu, vyhledejte aplikaci na webu [make.powerapps.com](https://make.powerapps.com) a pak se podívejte do pole **ID aplikace** pod položkou **Podrobnosti**.
    - Pro **Vstupní kontext pro aplikaci** lze volitelně vybrat pole obsahující data, která je nutné předat do aplikace jako vstup. Dále v pozdější části tohoto tématu [Vytvoření aplikace, která využívá data odeslaná z aplikací Finance and Operations](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) získáte podrobné informace o přístupu aplikace k datům odeslaným z aplikací Finance and Operations.
    - Zvolte **velikost aplikace** odpovídající typu aplikace, kterou vkládáte. Vyberte **Tenký** pro aplikace vytvořené pro mobilní zařízení a **Široký** pro aplikace vytvořené pro tablety. To zajišťuje, že je pro integrovanou aplikaci vyhrazeno dostatečné množství místa.
    - Pevná záložka **Právnické osoby** poskytuje možnost zvolit, pro jaké právnické osoby je aplikace dostupná. Výchozí nastavení je učinit aplikaci přístupnou všem právnickým osobám. Tato možnost je k dispozici pouze tehdy, je-li zakázána funkce [uložená zobrazení](saved-views.md). 

4. Po potvrzení správnosti konfigurace klepněte na tlačítko **Vložit** pro vložení PowerApp na stránku. Budete vyzváni k obnovení prohlížeče, aby se zobrazila integrovaná aplikace.

## <a name="sharing-an-embedded-app"></a>Sdílení integrované aplikace

Po vložení aplikace plátna na stránku a ověření, že pracuje správně v jakémkoli kontextu dat předaném ze stránky můžete sdílet tuto vloženou aplikaci s ostatními uživateli v systému. Chcete-li sdílet vloženou aplikaci plátna, postupujte takto.

1. [Sdílejte aplikaci plátna](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) s příslušnými uživateli, aby měli přístup k aplikaci v Power Apps. 

2. Ujistěte se, že cíloví uživatelé mají příslušná přizpůsobení, aby se vložená aplikace zobrazila, když tito uživatelé zobrazí stránku. Můžete použít některý z následujících způsobů.

    - Doporučeno: Použijte funkci [Uložená zobrazení](saved-views.md) pro vytvoření a publikování zobrazení, které obsahuje vloženou aplikaci. Tento způsob zajišťuje, že aplikaci uvidí všichni uživatelé, kteří mají role zabezpečení, na které se cílí publikované zobrazení aplikace Finance and Operations. 
    - Pokud nemáte zapnutou funkci Uložená zobrazení, můžete nechat správce systému odeslat personalizaci, která zahrnuje vloženou aplikaci všem uživatelům nebo podmnožině uživatelů. Případně můžete exportovat přizpůsobení své stránky a odeslat je jednomu nebo více uživatelům. Každý z těchto uživatelů pak může importovat personalizace. Panel nástrojů individuálního nastavení obsahuje akce, které vám umožní exportovat a importovat individuální nastavení. 
    
> [!NOTE]
> Pokud byla aplikace plátna sdílena s externími uživateli, nemohou tito uživatelé použít vloženou aplikaci uvnitř aplikace Finance and Operations. Mohou však přistupovat k aplikaci přímo uvnitř Power Apps. Externí uživatelé zahrnují hosty a uživatele, kteří nepatří do Microsoft 365 Azure Directory, kde je aplikace Finance and Operations nasazena.

Podrobnější informace o možnostech přizpůsobení v produktu a jejich použití naleznete v tématu [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Vytváření aplikace plátna, která používá data odesílaná z aplikací Finance and Operations

Když vytvoříte aplikaci plátna, která bude vložena do aplikace Finance and Operations, jednou důležitou součástí procesu je použití vstupních dat z této aplikace Finance and Operations. Z vývojového prostředí Power Apps lze vstupní data předaná z Finance and Operations otevřít pomocí proměnné **Param("EntityId")**.

Například ve funkci Při spuštění aplikace můžete nastavit vstupní data z aplikací Finance and Operations do proměnné následujícím způsobem:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Prohlížení aplikace plátna

Chcete-li zobrazit vloženou aplikaci plátna na stránce v aplikacích Finance and Operations, jednoduše přejděte na stránku s vloženou aplikací. Nezapomeňte, že k aplikacím lze přistupovat pomocí tlačítka **Power Apps** ve standardním podokně akcí. Alternativně se mohou objevit přímo na stránce jako nová karta, záložku s náhledem, okno nebo nový oddíl v pracovním prostoru. Když se uživatelé poprvé pokusí načíst aplikaci na stránku, budou vyzváni k přihlášení. Tento krok zajišťuje, že uživatelé mají příslušná oprávnění k používání aplikace.

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