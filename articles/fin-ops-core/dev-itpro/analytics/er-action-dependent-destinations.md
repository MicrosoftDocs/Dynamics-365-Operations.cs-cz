---
title: Konfigurace cílů ER závislých na akci
description: Toto téma vysvětluje, jak konfigurovat cíle závislé na akcích formátu elektronického výkaznictví (ER), který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d860c2b9fe01231e8e47b085f93c79c5a7dc449e
ms.sourcegitcommit: d13ea8b6baf73601a8b57548232aac84ffaba717
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7941237"
---
# <a name="configure-action-dependent-er-destinations"></a>Konfigurace cílů ER závislých na akci

[!include [banner](../includes/banner.md)]

Můžete konfigurovat [cíle](electronic-reporting-destinations.md) pro každou výstupní komponentu (složku nebo soubor) [elektronického výkaznictví (ER)](general-electronic-reporting.md) [formát](general-electronic-reporting.md#FormatComponentOutbound) [konfigurace](general-electronic-reporting.md#Configuration) který se používá pro generování odchozích dokumentů. Uživatelé, kteří používají formát tohoto typu ER a mají příslušná přístupová práva, mohou také změnit nakonfigurované nastavení cíle za běhu.

V Microsoft Dynamics 365 Finance **verze 10.0.17 a novější** lze spustit formát ER pomocí [zajišťování](er-apis-app10-0-17.md) kódu akce, který uživatel provede spuštěním daného formátu ER. Například v modulu **Pohledávky** v nastavení správy tisku můžete vybrat formát ER, který generuje konkrétní obchodní dokument, například fakturu s volným textem. Poté můžete vybrat **Zobrazit** k zobrazení náhledu faktury nebo **Vytisknout** pro odeslání na tiskárnu. Pokud je za běhu předána akce uživatele pro spuštěný formát ER, můžete nakonfigurovat různé cíle ER pro různé akce uživatele. Toto téma vysvětluje, jak konfigurovat cíle ER pro tento typ formátu ER.

## <a name="make-action-dependent-er-destinations-available"></a>Zpřístupnění cílů ER závislých na akcích

Chcete-li konfigurovat cíle ER závislé na akci v aktuální instanci Finance a povolit [nové](er-apis-app10-0-17.md) rozhraní ER API, otevřete pracovní prostor [Správa funkcí](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) a zapněte funkci **Konfigurovat konkrétní cíle ER, které se mají použít pro různé akce PM**. Chcete-li použít nakonfigurované cíle ER pro [konkrétní](#reports-list-wave1) sestavy za běhu, povolte funkci **Směrovat výstup sestav PM na základě cílů ER, které jsou specifické pro konkrétní akci uživatele (vlna 1)**.

## <a name="configure-action-dependent-er-destinations"></a>Konfigurace cílů ER závislých na akci

Když zapnete funkci **Konfigurovat konkrétní cíle ER na použití pro různé akce PM**, můžete nakonfigurovat cíle ER závislé na akci na kartě s náhledem **Cíl souboru** stránky **Cíl elektronického výkaznictví**. Pro každou komponentu můžete přidat záznam a povolit konkrétní cíle ER. U každého záznamu musíte určit typ dokumentu, pro který by se měly použít nakonfigurované cíle ER. V poli **Typ dokumentu** vyberte některou z následujících hodnot:

- Vyberte **Elektronický**, chcete-li použít nakonfigurované cíle, pokud za běhu není poskytnut žádný uživatelský akční kód.
- Vyberte **Správa tisku**, chcete-li použít nakonfigurované cíle, pokud za běhu je poskytnut uživatelský akční kód.
- Vyberte **Libovolný**, chcete-li vždy použít nakonfigurované cíle, bez ohledu na to, zda je za běhu poskytnut uživatelská akce.

Pokud vyberete typ dokumentu **Správa tisku**, musíte určit akce uživatele, na které mají být aplikovány konfigurované cíle ER. V poli **Akce správy tisku** vyberte některou z následujících hodnot:

- Vyberte **Zobrazení**, chcete-li použít nakonfigurované cíle, pokud za běhu není poskytnuta žádná akce uživatele **Zobrazení**.
- Vyberte **Tisk**, chcete-li použít nakonfigurované cíle, pokud za běhu není poskytnuta žádná akce uživatele **Tisk**.
- Vyberte **Odeslat**, chcete-li použít nakonfigurované cíle, pokud za běhu není poskytnuta žádná akce uživatele **Odeslat**.

> [!NOTE]
> Pro jeden záznam cíle lze vybrat více akcí.

Pokud vyberete typ dokumentu **Žádný**, je automaticky vybrána **Auto detekce** v poli **Akce správy tisku** pole jako akce uživatele a dojde k následujícímu chování:

- Pokud není v době běhu poskytnut kód akce uživatele, použijí se všechny nakonfigurované cíle ER.
- Pokud je uživatelský akční kód poskytnut za běhu, použije se cíl ER, který je předdefinován pro konkrétní akci, **bez ohledu na to, zda byla povolena**:

    - Když je za běhu poskytnuta akce **Zobrazení**, použije se cíl ER **Obrazovka**.
    - Když je za běhu poskytnuta akce **Odeslat**, použije se cíl ER **E-mail**.
    - Když je za běhu poskytnuta akce **Tisk**, použije se cíl ER **Tiskárna**.

Můžete například použít formát ER **volná textová faktura (Excel)**, pokud chcete vytisknout [volnou textovou fakturu](../../../finance/accounts-receivable/create-free-text-invoice-new.md) při zaúčtování. Chcete-li směrovat vygenerovaný dokument, musíte nakonfigurovat cíle ER pro tento formát ER. Možná budete muset nakonfigurovat tyto cíle ER, aby na generovaném dokumentu provedly následující:

- Archivujte dokument, pokud je spuštěn formát ER, ale není poskytnut žádný kód akce (například když je dokument odeslán elektronicky).
- Náhled dokumentu ve webovém prohlížeči, když uživatel provede akci **Zobrazení** .
- Archivujte a vytiskněte dokument, když uživatel provede akci **Vytisknout**.
- Archivujte dokument a odešlete jej e-mailem jako přílohu odchozí e-mailové zprávy, když uživatel provede akci **Poslat**.

Následující obrázek ukazuje, jak můžete dosáhnout této konfigurace cílů ER jako sady individuálních záznamů o cíli, když je každý záznam nakonfigurován pro jednotlivou akci uživatele:

![Cílová stránka elektronického hlášení, která má nastavení cíle závislé na akci pro formát ER, když je každý záznam cíle nakonfigurován pro jednu akci uživatele.](./media/er-destination-action-dependent-01.png)

Následující obrázek ukazuje, jak můžete dosáhnout stejné alternativní konfigurace cílů ER jako sady individuálních záznamů o cíli, když je každý záznam nakonfigurován pro jednotlivý cíl:

![Cílová stránka elektronického hlášení, která má nastavení cíle závislé na akci pro formát ER, když je každý záznam cíle nakonfigurován pro jeden cíl.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Pokud je pro spuštěný formát ER poskytnut kód akce, ale pro tento kód akce nebyly nakonfigurovány žádné cíle, je použito chování [výchozího](electronic-reporting-destinations.md#default-behavior) cíle.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Změna cílů ER závislých na akcích v době běhu

Při spuštění formátu ER, pokud byly akce uživatelů zřízeny uživateli, kteří mají příslušné [oprávnění](electronic-reporting-destinations.md#security-considerations), chcete-li změnit nakonfigurované nastavení cíle za běhu, zobrazí se dialogové okno s možností změnit nakonfigurované nastavení cíle. Toto dialogové okno je volitelné a jeho vzhled závisí na tom, jak bylo implementováno volání ER rámce pro spuštění formátu ER. Pokud se zobrazí toto dialogové okno, budou cíle ER v něm povoleny podle poskytované akce uživatele.

Následující obrázek ukazuje příklad dialogového okna **Cíle formátu elektronického výkaznictví**, které se zobrazí při [zaúčtování](../../../finance/accounts-receivable/create-free-text-invoice-new.md) volné textové faktury a je spuštěn formát ER **Volná textová faktura (Excel)** ke generování tohoto dokumentu, pokud byla zřízena akce **Tiskárna** a cíle ER byly pro tento formát nakonfigurovány, jak je uvedeno dříve v tomto tématu.

![Dialogové okno, které umožňuje změnit původně nakonfigurované cíle ER pro spuštěný formát ER.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Pokud jste nakonfigurovali cíle ER pro několik komponent běžícího formátu ER, bude nabídnuta možnost samostatně pro každou nakonfigurovanou komponentu formátu ER.

## <a name="verify-the-provided-user-action"></a>Ověření poskytnuté akce uživatele

Když provedete konkrétní akci uživatele, můžete ověřit, která akce uživatele, pokud existuje, je poskytována pro spuštěný formát ER. Toto ověření je důležité, když musíte nakonfigurovat cíle ER závislé na akci, ale nejste si jisti, jaký kód akce uživatele, pokud existuje, je poskytnut. Například když začnete účtovat volnou textovou fakturu a nastavíte možnost **Tisk faktury** na **Ano** v poli **Zaúčtovat volnou textovou fakturu**, můžete nastavit možnost **Použít cíl správy tisku** na **Ano** nebo **Ne**.

Pomocí těchto kroků ověřte poskytnutý kód akce uživatele.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** [nastavte](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) u možnosti **Spustit v režimu ladění** možnost **Ano**.
4. Proveďte akci uživatele spuštěním formátu ER. Uvědomte si, že parametry uživatele ER jsou specifické pro uživatele a konkrétní společnost.
5. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurovat protokoly ladění**.
6. Na stránce **Protokoly ladění konfigurace** filtrujte protokoly běhu ER a vyhledejte protokol pro běh ve formátu ER.
7. Zkontrolujte položky protokolu, které musí obsahovat záznam, který představuje poskytnutý kód akce uživatele, pokud byla poskytnuta nějaká akce pro spuštění formátu ER.

    ![Stránka s protokoly běhu elektronického výkaznictví, která obsahuje informace o kódu akce uživatele, který byl poskytnut pro filtrovaný běh formátu ER.](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Seznam obchodních dokumentů (vlna 1)</a>

Následující seznam obchodních dokumentů je řízen funkcí **Směrovat výstup zpráv PM na základě cílů ER, které jsou specifické pro konkrétní akci uživatele (vlna 1)**:

- Faktura odběratele (volná textová faktura)
- Faktura zákazníka (prodejní faktura)
- Nákupní objednávka
- Nákupní žádanka nákupní objednávky
- Prodejní objednávka – potvrzení
- Upomínka
- Oznámení úroků
- Poradenství ohledně plateb dodavatelům
- Požadavek na nabídku

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Změny rozhraní API architektury elektronického výkaznictví pro Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
