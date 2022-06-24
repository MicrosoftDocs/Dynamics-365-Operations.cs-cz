---
title: Vytvoření nového modulu správy přepravy
description: Tento článek popisuje, jak vytvořit nový modul správy přepravy v Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 627972ef6afb7551bb57821ded24183f8f335e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857250"
---
# <a name="create-a-new-transportation-management-engine"></a>Vytvoření nového modulu správy přepravy

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvořit nový modul správy přepravy v Dynamics 365 Supply Chain Management. 

Moduly správy přepravy (TMS) definují logiku, které slouží ke generování a zpracování přepravní sazby v rámci správy přepravy. Supply Chain Management poskytuje několik různých typů modulů, které vypočítávají různé parametry, jako jsou sazby, časy přepravy a počet zón, které budou během přepravy překročeny. Tento článek vysvětluje, jak používat vývojové prostředí Microsoft Visual Studio spolu s vývojovými nástroji Supply Chain Management k vytvoření a nasazení nového modulu TMS a následně jak nastavit modul v Operations. Více informací o motorech viz [Motory pro řízení dopravy](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Vytvoření nového modulu TMS

Tato část vysvětluje, jak vytvořit knihovnu tříd, která má implementaci modulu TMS, a jak na ni odkazovat z modelu Supply Chain Management.

1. Chcete-li nasadit své nové moduly, musíte mít model, který bude moduly obsahovat. V nabídce **Dynamics 365** &gt; **Správa modelu** klikněte na možnost **Vytvořit model** k vytvoření nového modelu. Na první stránce průvodce **Vytvořit model** pojmenujte model **TMSEngines**. 

   [![Vytvoření modelu.](./media/012.png)](./media/012.png)

2. Na další stránce vyberte **Vytvořit nový balíček**. 

   [![Vytvoření nového balíčku.](./media/021.png)](./media/021.png)

3. Na další stránce vyberte model **ApplicationSuite** k odkázání. (Model **ApplicationPlatform** je předem vybrán.) 

   [![Výběr modelu k odkázání.](./media/032.png)](./media/032.png)

4. Na další stránce klikněte na **Dokončit** pro potvrzení vytvoření nového modelu. 

   [![Dokončení tvorby modelu.](./media/042.png)](./media/042.png)

5. V novém řešení vytvořte nový projekt Supply Chain Management a pojmenujte ho **TMSThirdParty**. Ve vlastnostech projektu nastavte model projektu na **TMSEngines**.
6. Přidejte novou knihovnu tříd C\# k vašemu řešení a pojmenujte ji **ThirdPartyTMSEngines**.
7. V projektu ThirdPartyTMSEngines přidejte odkazy na specifická sestavení Supply Chain Management:
   -   Sestavení aplikací, které umožňují odkazovat na typy X++. Tato sestavení lze nalézt na následujících místech. \[Kořen balíčků\] je cesta k umístění, kde jsou umístěny všechny nasazené sestavy, například C:\\Packages.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Sestavy rámce, které umožňují přístup k datům, LINQ a pomocným funkcím. Všechna tato sestavení najdete v \[Kořen balíčků\]\\bin.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Základní sestavení TMS (které obsahuje moduly) a základní sestavení TMS (které obsahuje pomocníky, konstanty, definice tříd přenosu dat atd.). Tato sestavení lze nalézt na následujících místech.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Přejmenujte třídu C\#, která je automaticky vygenerována v projektu ThirdPartyTMSEngines na **SampleRatingEngine**.
9. Implementujte modul. Protože v tomto příkladu vytváříme modul přepravních sazeb, dědíme ze základní třídy pro moduly přepravních sazeb. Základní třída implementuje většinu rozhraní modulu přepravních sazeb (**TMSFwkIRateEngine**). Musíme jen implementovat metodu sazby. Aby byl tento příklad jednoduchý, učiníme tuto metodu registrací pevně zakódované sazby 100. Můžete vytvořit motory, které implementují jakékoli rozhraní modulu, jako např. **TMSFwkIAccessorialEngine**. Všechna rozhraní modulu jsou definována v X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Sestavte řešení.
11. Přidejte nový odkaz na projekt TMSThirdParty. Odkaz musí ukazovat na projekt ThirdPartyTMSEngines. Po dokončení by vaše řešení mělo vypadat takto. 

    [![Řešení, které obsahuje odkaz na projekt TMSThirdParty.](./media/052.png)](./media/052.png)

12. Sestavte řešení. Ověřte, že se nová knihovna objeví v uzlu **Reference** v Průzkumníku aplikací. 

    [![Nová knihovna v uzlu Reference průzkumníku aplikací.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Nasaďte modul TMS jako balíček

Jedním ze způsobů nasazení modulů TMS třetích stran je prostřednictvím balíčku nasazení. Tento přístup se doporučuje v produkčním prostředí. Ve vývojovém prostředí můžete ručně zkopírovat sestavení, jak je popsáno v další části „Nastavení modulu TMS v Supply Chain Management“. Pokud chcete nasadit modul jako balíček, postupujte takto.

1. V nabídce **Dynamics 365** &gt; **Nasadit** klikněte na <strong>Vytvořit balíček nasazení</strong>.
2. V dialogovém okně **Vytvořit balíček nastavení** vyberte model TMSEngines a zadejte cestu, kam chcete uložit soubory balíčků. 

   [![Výběr modelu TMSEngines.](./media/071.png)](./media/071.png)

3. Nyní můžete nasadit balíček do cílového prostředí. Návod viz [Instalace nasaditelného balíčku](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Nastavení modulu TMS v Supply Chain Management

Tato část vysvětluje, jak nastavit Supply Chain Management pro použití modulu TMS, a ukazuje, jak se nový modul, který jsme vytvořili, používá při návrhu přepravních sazeb. Příklad v této části ukázkovou datovou společnost USMF.

1. Vytvořte nový modul, jak je popsáno v části „Vytvoření nového modulu TMS“.
2. Sestavte řešení.
3. Zkopírujte výslednou sestavu do binárního umístění serveru Supply Chain Management, \[AOSWebRoot\]bin. **Poznámka:** Tento krok je relevantní pouze ve vývojovém prostředí. V produkčním prostředí byste měli nasadit prostřednictvím balíčku nasazení. Pokyny naleznete v předchozí části „Nasazení modulu TMS jako balíčku“.
4. V Supply Chain Management na stránce **Moduly přepravních sazeb** vytvořte nový modul přepravních sazeb. Modul by měl ukazovat na sestavu modulu, která je vytvořena vytvořením knihovny tříd modulu a třídy modulu, kterou jste implementovali. 

   [![Vytvoření nového modulu přepravních sazeb na stránce Moduly přepravních sazeb.](./media/081.png)](./media/081.png)

5. Vytvořte přepravce, který používá vzorový modul přepravních sazeb. Protože náš modul nepoužívá žádná data, nemusíte přiřazovat hlavní sazbu. 

   [![Vytvoření nového dopravce.](./media/092.png)](./media/092.png)

6. Na stránce **Workbench cesty sazby** klikněte na **Návrh sazeb**. Měli byste vidět sazbu 100,00 od SampleCarrier, jak je znázorněno na následujícím snímku obrazovky. V tomto příkladu navrhujeme sazby na trase ze skladu 24 k zákazníkovi US-004. Protože je však sazba pevně zakódována, vždy uvidíte sazbu 100,00.

   [![Pracovní plocha sazeb trasy.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Tipy

- Pokud používáte vývojové nástroje pro Supply Chain Management, je užitečné přidat do řešení nový projekt. Pokud nastavíte tento projekt jako svůj spouštěcí projekt a spustíte relaci ladění, můžete ladit kód X++ i C\# ve stejné relaci ladění.
- Pokaždé, když změníte a znovu zkompilujete svůj projekt ThirdPartyTMSEngines, musíte výsledné sestavení ručně zkopírovat do binárního umístění nebo nasadit prostřednictvím balíčku nasazení. V opačném případě můžete spustit pomocí zastaralé sestavy.
- Po provedení operací specifických pro TMS v Supply Chain Management může pracovní proces Internetové informační služby (IIS) uzamknout sestavení ThirdPartyTMSEngines, takže sestavení nebude možné aktualizovat. V tomto případě restartujte proces w3svc.

### <a name="whitepaper"></a>Dokument Whitepaper

Chcete-li získat další informace, stáhněte si následující dokument whitepaper (napsaný na podporu AX2012, ale stále platí pro Dynamics 365 Supply Chain Management)

- [Implementace a nasazení modulu pro řízení přepravy](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]