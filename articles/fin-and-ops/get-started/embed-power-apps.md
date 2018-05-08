---
title: "Vložené PowerApps"
description: "Toto téma popisuje způsob vložení PowerApps do klienta Finance and Operations pro zvýšení funkčnosti produktu."
author: jasongre
manager: AnnBe
ms.date: 04/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>Vložené PowerApps

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pre-release.md)]

V aktualizaci Platformy 14, Microsoft Dynamics 365 for Finance and Operations podporuje integraci s Microsoft PowerApps, službou pro vývojáře a netechnické uživatele pro vytváření vlastních obchodních aplikací pro mobilní zařízení, tablety a web bez zápisu kódu. PowerApps, které jste vytvořili vy, vaše organizace nebo širší ekosystém, lze poté vložit do klienta Finance and Operations, aby bylo možné vylepšit funkce produktu. Například může vytvořit PowerApp pro doplnění modulu Finance and Operations informacemi získanými z jiného systému. 

Další informace o začlenění PowerApps se dozvíte v krátkém videu [Jak začlenit PowerApps do Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY) grafické.

> [!Video https://www.youtube.com/embed/x3qyA1bH-NY]

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Přidání vložené PowerApp na stránku
### <a name="overview"></a>Přehled
Před vložením PowerApp do klienta Finance and Operations, je nejdříve nutné najít nebo vytvořit PowerApp s požadovanými vizuály nebo funkcemi. Nepopíšeme zde podrobný proces vytváření PowerApp. Téma [Úvod do PowerApps](https://docs.microsoft.com/en-us/powerapps/getting-started) je ideálním výchozím bodem, pokud s PowerApps začínáte.

Až budete připraveni integrovat konkrétní PowerApp, můžete si vybrat mezi dvěma způsoby přístupu k PowerApp na stránce, podle toho, který postup lépe vyhovuje vašim potřebám. První způsob je pomocí tlačítka PowerApps, které bylo přidáno do standardního podokna akcí. PowerApps přidané pomocí tohoto mechanismu se budou zobrazovat jako položky nabídky uvnitř tlačítka nabídky PowerApps. Jsou-li vybrané, otevřou všechny tyto položky nabídky podokno obsahující vloženou PowerApp. Alternativně se můžete rozhodnout rovněž zobrazit PowerApp přímo na stránce jako novou kartu, pevnou záložku, list nebo nový oddíl v pracovním prostoru. 

Při konfiguraci vaší integrované PowerApp v aplikaci Finance and Operations, můžete vybrat jednoho pole, které má být odesláno jako vstup do PowerApp. To umožňuje, aby PowerApp reagovala na základě dat, které se aktuálně zobrazují v aplikaci Finance and Operations.  

### <a name="details"></a>Podrobnosti
Následující pokyny popisují postup integrace PowerApp do webového klienta aplikace Finance and Operations.  

1. Přejděte na stránku, kam chcete vložit PowerApp. Bude se jednat o stejnou stránku, která obsahuje všechna data potřebná k předání do PowerApp jako vstup.  
2. Otevřete podokno **Vložit PowerApp**:
   - Klepněte na tlačítko **možnosti** a poté vyberte **přizpůsobit tento formulář**. V nabídce **Vložit** zvolte **PowerApp**. Nakonec vyberte oblast, kam chcete přidat PowerApp. Pokud se má vložit PowerApp pod tlačítkem nabídky PowerApps, vyberte podokno akcí. Pokud se má vložit PowerApp přímo na stránku, zvolte příslušnou kartu, pevnou záložku, list nebo oddíl (pokud jste v pracovním prostoru).   
   - Pokud bude do PowerApp získán přístup pomocí tlačítka nabídky PowerApps, můžete rovněž klepnout na tlačítko nabídky **PowerApps** v podokně akcí a poté vybrat **vložit PowerApp**.  
3. Konfigurace vložené PowerApp:
   - Pole **Název** označuje text zobrazený pro tlačítko nebo kartu, které budou obsahovat integrovanou PowerApp. Často můžete chtít opakovat název PowerApp v tomto poli.  
   - **ID aplikace** je identifikátor GUID pro PowerApp, který má být vložen. Chcete-li načíst tuto hodnotu, vyhledejte PowerApp na [web.powerapps.com](https://web.powerapps.com) a vyhledejte pole **ID aplikace** pod položkou **Podrobnosti**.  
   - Pro **vstupní data pro PowerApp** lze volitelně vybrat pole obsahující data, která je nutné předat do PowerApp jako vstup. Podrobné informace o přístupu PowerApp k datům odeslaným z aplikace Finance and Operations naleznete v části tohoto tématu nazvané [Vytvoření PowerApp, která využívá data z Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations).  
   - Zvolte **velikost aplikace** odpovídající typu PowerApp, který vkládáte. Vyberte **Tenký** pro aplikace PowerApps vytvořené pro mobilní zařízení a **Široký** pro PowerApps vytvořené pro tablety. To zajišťuje, že je pro integrovanou PowerApp vyhrazeno dostatečné množství místa.
   - Pevná záložka **Právnické osoby** poskytuje možnost zvolit, pro jaké právnické osoby je PowerApp dostupná. Výchozí nastavení je pro zobrazení PowerApp ve všech právnických osobách.  
4. Po potvrzení správnosti konfigurace klepněte na tlačítko **Vložit** pro vložení PowerApp na stránku. Budete vyzváni k obnovení prohlížeče, aby se zobrazila integrovaná PowerApp. 

## <a name="sharing-an-embedded-powerapp"></a>Sdílení integrované PowerApp
Po vložení PowerApp na stránku a ověření, že pracuje správně v jakémkoli kontextu dat předaném ze stránky můžete sdílet tuto vloženou PowerApp s ostatními uživateli v systému. Toho lze dosáhnout dvěma různými způsoby pomocí možností individuálního nastavení produktu:

- Doporučený scénář je prostřednictvím správce systému, který může individuální nastavení předat všem uživatelům nebo podmnožině uživatelů. 

- Případně můžete exportovat přizpůsobení své stránky, zaslat je jednomu nebo více uživatelům a nechat tyto jednotlivé uživatelé importovat vaše změny. Možnost Spravovat na panelu nástrojů induviduálního nastavení vám umožní exportovat a importovat individuální nastavení.

Podrobnější informace o možnostech přizpůsobení v produktu a jejich použití naleznete v tématu [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Vytváření PowerApp, která využívá data odeslaná z Finance and Operations
Důležitou část vytváření PowerApp, které budou vloženy do modulu Finance and Operations je používání vstupních dat z modulu Finance and Operations. Uvnitř PowerApp lze k těmto vstupním datům získat přístup proměnné Param("EntityId").  

Například ve funkci Při spuštění PowerApp můžete nastavit vstupní data z modulu Finance and Operations následujícím způsobem:

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Zobrazení integrované PowerApp
Chcete-li zobrazit integrovanou PowerApp na stránce v aplikaci Finance and Operations, jednoduše přejděte na stránku s integrovanou PowerApp. Vzpomeňte si. že k PowerApps lze přistupovat prostřednictvím tlačítka PowerApps ve standardním podokně akcí, nebo se mohou zobrazit přímo na stránce jako nová karta, pevná záložka nebo jako nová část v pracovním prostoru. Když se uživatel pokusí načíst PowerApp na stránce poprvé, bude vyzván k přihlášení do PowerApps, aby se zajistilo, že má příslušná oprávnění k použití PowerApp.   

## <a name="editing-an-embedded-powerapp"></a>Úprava integrované PowerApp
Poté, co byla vložena PowerApp na stránku, je nutné provést změny v konfiguraci této PowerApp. Možná například chcete změnit popisek přidružené vložené PowerApp nebo byla vytvořena nová verze PowerApp a je nutné aktualizovat na poslední ID aplikace odkazující na PowerApp. 

Následovně můžete upravit konfiguraci vložených PowerApp:
1. Přejděte do podokna **Upravit PowerApp**. 
   - Je-li vložená PowerApp otevírána přes tlačítko nabídky PowerApps, klikněte pravým tlačítkem myši na tlačítko PowerApps a vyberte **přizpůsobit**. Vyberte PowerApp, kterou chcete konfigurovat z rozevírací nabídky **Zvolit PowerApp**.  
   - Pokud se vložená PowerApp zobrazí přímo na stránce, vyberte **Možnosti** a potom **Přizpůsobit tento formulář**. S použitím nástroje **Vybrat** klikněte na integrovanou PowerApp.  
2. Proveďte potřebné změny konfigurace PowerApps a klepněte na tlačítko **Uložit**.  

## <a name="removing-an-embedded-powerapp"></a>Odstranění integrované PowerApp
Poté, co byla vložena PowerApp na stránku, existují dva způsoby, jak ji odebrat v případě potřeby: 

- Přejděte do podokna **Upravit PowerApp** podle pokynů v části [Úpravy vložené PowerApp](#editing-an-embedded-powerapp) dříve v tomto tématu. Potvrďte, že se v podokně zobrazí informace o vložené PowerApp, kterou chcete odebrat, a klepněte na tlačítko **odstranit**. 

- Vzhledem k tomu, že vložená PowerApp je uložena jako údaj o individuálním nastavení, clearing přizpůsobení stránky rovněž odstraní všechny PowerApps vložené na této stránce. Poznámka: zrušení zaškrtnutí přizpůsobení stránky je trvalé a nelze je vrátit zpět. Chcete-li odebrat vaše individuální nastavení na stránce, vyberte **Možnosti** a klikněte na **Přizpůsobit tento formulář**. V nabídce **Spravovat** zvolte tlačítko **Vymazat**. Po aktualizaci prohlížeče budou odebrána všechna předchozí individuální nastavení pro tuto stránku. Další informace o optimalizaci stránek pomocí individuálního nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).  

## <a name="appendix"></a>Dodatek 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Vývojář může kontrolovat, kam lze PowerApp vložit.
Podle výchozího nastavení uživatel může vložit PowerApps na každou stránku pod tlačítkem nabídky PowerApps nebo přímo na stránku jako kartu, pevnou záložku, list nebo jako nový oddíl v pracovním prostoru. Avšak v případě potřeby vývojáři také mohou konfigurovat tuto funkci, aby povolila vnoření PowerApps pouze na některé stránky pomocí následujících metod: 

- **isPowerAppPersonalizationEnabled** - Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, pak tlačítko nabídky PowerApps nebude zobrazeno a uživatelé nebudou moci vkládat PowerApps kamkoli na tuto stránku, včetně karty. 

- **isPowerAppTabPersonalizationEnabled** - Pokud tato metoda vrátí hodnotu false pro konkrétní stránku, potom uživatelé nebudou moci vkládat PowerApps přímo na stránku jako kartu, pevnou záložku nebo oddíl panoramatu. Uživatelé budou moci vložit PowerApps pomocí tlačítka nabídky PowerApps, je-li vkládání na stránce povoleno.  

Následující příklad ukazuje novou třídu s dvěma metodami potřebnými ke konfigurace, kde má být PowerApps vložena.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


