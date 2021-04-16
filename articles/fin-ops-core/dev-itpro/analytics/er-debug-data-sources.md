---
title: Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace
description: Toto téma vysvětluje, jak můžete ladit zdroje dat prováděného formátu ER, aby bylo možné lépe porozumět nakonfigurovanému toku dat a transformaci.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fe3e6a4223fc8b26e523a982a2e1752a34b370de
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753665"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="76e48-103">Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace</span><span class="sxs-lookup"><span data-stu-id="76e48-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="76e48-104">Když [konfigurujete](tasks/er-format-configuration-2016-11.md) řešení elektronického výkaznictví (ER) ke generování odchozích dokumentů, definujete metody, které se používají k získání dat mimo aplikaci a jejich zadání do generovaného výstupu.</span><span class="sxs-lookup"><span data-stu-id="76e48-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="76e48-105">Aby byla podpora životního cyklu řešení ER efektivnější, mělo by vaše řešení sestávat z [datového modelu](general-electronic-reporting.md#DataModelComponent) a jeho komponent [mapování](general-electronic-reporting.md#ModelMappingComponent) a také z [formátu](general-electronic-reporting.md#FormatComponentOutbound) ER a jeho komponent mapování, tak, aby mapování modelu bylo specifické pro aplikaci, zatímco ostatní komponenty zůstaly pro aplikaci agnostické.</span><span class="sxs-lookup"><span data-stu-id="76e48-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="76e48-106">Proto může několik komponent ER [ovlivnit](general-electronic-reporting.md#FormatComponentOutbound) proces zadávání dat do generovaného výstupu.</span><span class="sxs-lookup"><span data-stu-id="76e48-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="76e48-107">Někdy vypadají data generovaného výstupu odlišně od stejných dat v aplikační databázi.</span><span class="sxs-lookup"><span data-stu-id="76e48-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="76e48-108">V těchto případech budete chtít určit, která komponenta ER je zodpovědná za transformaci dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="76e48-109">Funkce ladicího programu zdroje dat ER významně snižuje čas a náklady, které jsou zahrnuty v tomto šetření.</span><span class="sxs-lookup"><span data-stu-id="76e48-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="76e48-110">Můžete přerušit provádění formátu ER a otevřít rozhraní ladicího programu zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="76e48-111">Zde můžete procházet dostupné zdroje dat a vybrat individuální zdroj dat pro provedení.</span><span class="sxs-lookup"><span data-stu-id="76e48-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="76e48-112">Toto ruční provedení simuluje spuštění zdroje dat během skutečného spuštění formátu ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="76e48-113">Výsledek je uveden na stránce, kde můžete analyzovat přijatá data.</span><span class="sxs-lookup"><span data-stu-id="76e48-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="76e48-114">Chcete-li zapnout funkci ladění zdroje dat, nastavte možnost **Povolit ladění dat při spuštění formátu** na **Ano** v uživatelských parametrech ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="76e48-115">Poté můžete spustit ladění zdroje dat při spuštění formátu ER pro generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="76e48-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="76e48-116">Také můžete pomocí možnosti **Spustit ladění** zahájit ladění zdroje dat pro formát ER, který je nakonfigurován v [Návrháři operací ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="76e48-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="76e48-117">Toto téma poskytuje pokyny k zahájení ladění zdroje dat pro spuštěné formáty ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="76e48-118">Vysvětluje, jak vám tyto informace mohou pomoci pochopit tok dat a jejich transformace.</span><span class="sxs-lookup"><span data-stu-id="76e48-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="76e48-119">Příklady v tomto tématu používají obchodní proces pro zpracování plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="76e48-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="76e48-120">Omezení</span><span class="sxs-lookup"><span data-stu-id="76e48-120">Limitations</span></span>

<span data-ttu-id="76e48-121">Ladicí program zdroje dat lze použít pro přístup k datům zdrojů dat, které se používají ve formátech ER, které jsou spouštěny pro generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="76e48-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="76e48-122">Nelze jej použít k ladění zdrojů dat formátů ER, které jsou navrženy k analýze příchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="76e48-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="76e48-123">Následující nastavení formátů ER aktuálně nejsou k dispozici pro ladění zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="76e48-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="76e48-124">Transformace formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-124">Format transformations</span></span>
- <span data-ttu-id="76e48-125">Pravidla ověření formátování a mapování</span><span class="sxs-lookup"><span data-stu-id="76e48-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="76e48-126">Povolení výrazů</span><span class="sxs-lookup"><span data-stu-id="76e48-126">Enabling expressions</span></span>
- <span data-ttu-id="76e48-127">Podrobnosti o sběru dat v paměti</span><span class="sxs-lookup"><span data-stu-id="76e48-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="76e48-128">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="76e48-128">Prerequisites</span></span>

- <span data-ttu-id="76e48-129">Abyste mohli dokončit příklady v tomto tématu, musíte mít přístup k některé z následujících [rolí](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="76e48-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="76e48-130">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="76e48-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="76e48-131">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="76e48-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="76e48-132">Správce systému</span><span class="sxs-lookup"><span data-stu-id="76e48-132">System administrator</span></span>

- <span data-ttu-id="76e48-133">Společnost musí být nastavena na **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="76e48-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="76e48-134">Podle pokynů v [příloze 1](#appendix1) tohoto tématu si stáhněte součásti řešení Microsoft ER, které jsou potřeba ke zpracování plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="76e48-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="76e48-135">Podle pokynů v [příloze 2](#appendix2) tohoto tématu připravte pohledávky na zpracování platby dodavatele pomocí řešení ER, které si stáhnete.</span><span class="sxs-lookup"><span data-stu-id="76e48-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="76e48-136">Zpracování platby dodavatele pro účely získání souboru platby</span><span class="sxs-lookup"><span data-stu-id="76e48-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="76e48-137">Platby dodavatele zpracujte podle kroků v [příloze 3](#appendix3) tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="76e48-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Probíhá zpracování plateb dodavatele](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="76e48-139">Stáhněte a uložte soubor zip do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="76e48-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="76e48-140">Extrahujte soubor platby **ISO20022 Credit transfer.xml** ze souboru zip.</span><span class="sxs-lookup"><span data-stu-id="76e48-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="76e48-141">Otevřete extrahovaný soubor platby pomocí prohlížeče souborů XML.</span><span class="sxs-lookup"><span data-stu-id="76e48-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="76e48-142">V souboru platby nemá kód IBAN (International Bank Account Number) bankovního účtu dodavatele žádné mezery.</span><span class="sxs-lookup"><span data-stu-id="76e48-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="76e48-143">Proto se liší od hodnoty, která byla [zadána](#enteredIBANcode) na stránce **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="76e48-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN kód bez mezer](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="76e48-145">Pomocí ladicího programu zdroje dat ER zjistíte, která složka řešení ER se používá ke zkrácení mezer v kódu IBAN.</span><span class="sxs-lookup"><span data-stu-id="76e48-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="76e48-146">Zapnutí ladění zdroje dat</span><span class="sxs-lookup"><span data-stu-id="76e48-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="76e48-147">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="76e48-148">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="76e48-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="76e48-149">Nastavte možnost **Povolit ladění dat při spuštění formátu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="76e48-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="76e48-150">Tento parametr je specifický pro uživatele a konkrétní společnost.</span><span class="sxs-lookup"><span data-stu-id="76e48-150">This parameter is user-specific and company-specific.</span></span>

    ![Dialogové okno Parametry uživatele](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="76e48-152">Zpracovat platbu dodavatele pro ladění</span><span class="sxs-lookup"><span data-stu-id="76e48-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="76e48-153">Platby dodavatele zpracujte podle kroků v [příloze 3](#appendix3) tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="76e48-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="76e48-154">V okně zprávy vyberte **Ano** pro potvrzení, že chcete přerušit zpracování plateb dodavatele a místo toho spustit ladění zdrojů dat na stránce **Ladit zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="76e48-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Pole zprávy s potvrzením](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="76e48-156">Ladění zdrojů dat, které se používají při zpracování plateb</span><span class="sxs-lookup"><span data-stu-id="76e48-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="76e48-157">Ladění mapování modelu</span><span class="sxs-lookup"><span data-stu-id="76e48-157">Debug the model mapping</span></span>

1. <span data-ttu-id="76e48-158">Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Mapování modelu** pro zahájení ladění z této komponenty ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="76e48-159">V podokně zdroje dat vlevo vyberte zdroj dat **\$notSentTransactions** zdroj dat a poté vyberte možnost **Přečíst všechny záznamy**.</span><span class="sxs-lookup"><span data-stu-id="76e48-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="76e48-160">Můžete vybrat volbu **Přečíst 1 záznam**, **Přečíst 10 záznamů**, **Přečíst 100 záznamů** nebo **Přečíst všechny záznamy** pro vynucení odpovídajícího počtu záznamů, které mají být načteny z vybraného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="76e48-161">Tímto způsobem můžete simulovat přístup ke zdroji dat z běžícího formátu ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="76e48-162">V podokně dat vpravo vyberte **Rozbalit vše**.</span><span class="sxs-lookup"><span data-stu-id="76e48-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="76e48-163">Vidíte, že vybraný zdroj dat typu **Seznam záznamů** obsahuje jeden záznam.</span><span class="sxs-lookup"><span data-stu-id="76e48-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="76e48-164">Rozbalte zdroj dat **\$notSentTransactions** a vyberte vnořenou metodu **vendBankAccountInTransactionCompany ()**.</span><span class="sxs-lookup"><span data-stu-id="76e48-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="76e48-165">Rozbalte metodu **vendBankAccountInTransactionCompany()** a vyberte vnořené pole **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="76e48-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="76e48-166">Vyberte **Získat hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="76e48-166">Select **Get value**.</span></span>

    <span data-ttu-id="76e48-167">Můžete vybrat **Získat hodnotu** pro vynucení čtení hodnoty vybraného pole vybraného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="76e48-168">Tímto způsobem můžete simulovat přístup do tohoto pole z běžícího formátu ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="76e48-169">Vyberte **Rozbalit vše**.</span><span class="sxs-lookup"><span data-stu-id="76e48-169">Select **Expand all**.</span></span>

    ![Hodnota pole IBAN v mapování modelu](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="76e48-171">Jak vidíte, mapování modelů není zodpovědné za zkrácené mezery, protože kód IBAN, který vrátí pro bankovní účet dodavatele, zahrnuje mezery.</span><span class="sxs-lookup"><span data-stu-id="76e48-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="76e48-172">Proto musíte pokračovat v ladění zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="76e48-173">Ladění mapování formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-173">Debug the format mapping</span></span>

1. <span data-ttu-id="76e48-174">Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Mapování formátu** pro pokračování v ladění z této komponenty ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="76e48-175">Vyberte zdroj dat **\$PaymentByDebtor** a poté vyberte **Přečíst všechny záznamy**.</span><span class="sxs-lookup"><span data-stu-id="76e48-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="76e48-176">Rozbalte **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="76e48-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="76e48-177">Rozbalte **\$PaymentByDebtor.Lines** a poté vyberte **Přečíst všechny záznamy**.</span><span class="sxs-lookup"><span data-stu-id="76e48-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="76e48-178">Rozbalte **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="76e48-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="76e48-179">Rozbalte **\$PaymentByDebtor.Lines.CreditorAccount.Identification** a vyberte **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="76e48-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="76e48-180">Vyberte **Získat hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="76e48-180">Select **Get value**.</span></span>
8. <span data-ttu-id="76e48-181">Vyberte **Rozbalit vše**.</span><span class="sxs-lookup"><span data-stu-id="76e48-181">Select **Expand all**.</span></span>

    ![Hodnota pole IBAN v mapování formátu](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="76e48-183">Jak vidíte, zdroje dat mapování formátu nejsou zodpovědné za zkrácené mezery, protože kód IBAN, který vrací pro bankovní účet dodavatele, zahrnuje mezery.</span><span class="sxs-lookup"><span data-stu-id="76e48-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="76e48-184">Proto musíte pokračovat v ladění zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="76e48-185">Ladění formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-185">Debug the format</span></span>

1. <span data-ttu-id="76e48-186">Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Formát** pro pokračování v ladění z této komponenty ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="76e48-187">Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** a pak vyberte **Přečíst všechny záznamy**.</span><span class="sxs-lookup"><span data-stu-id="76e48-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="76e48-188">Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** a pak vyberte **Přečíst všechny záznamy**.</span><span class="sxs-lookup"><span data-stu-id="76e48-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="76e48-189">Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** a pak vyberte **Získat hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="76e48-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="76e48-190">Vyberte **Rozbalit vše**.</span><span class="sxs-lookup"><span data-stu-id="76e48-190">Select **Expand all**.</span></span>

    ![Hodnota pole IBAN ve formátu](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="76e48-192">Jak vidíte, vázání formátu není zodpovědné za zkrácené mezery, protože kód IBAN, který vrátí pro bankovní účet dodavatele, zahrnuje mezery.</span><span class="sxs-lookup"><span data-stu-id="76e48-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="76e48-193">Proto je element **BankIBAN** nakonfigurován tak, aby používal transformaci formátu, která zkrátí mezery.</span><span class="sxs-lookup"><span data-stu-id="76e48-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="76e48-194">Zavřete ladicí program zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="76e48-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="76e48-195">Zkontrolujte transformace formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-195">Review the format transformations</span></span>

1. <span data-ttu-id="76e48-196">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="76e48-197">Na stránce **Konfigurace** vyberte **Platební model** \> **Převod kreditu ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="76e48-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="76e48-198">Vyberte **Návrhář** a pak rozbalte elementy pro výběr možností **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="76e48-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![Element BankIBAN na stránce Návrhář formátu](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="76e48-200">Jak vidíte, element **BankIBAN** je nakonfigurován na použití transformace **odstranit ne alfanumerické**.</span><span class="sxs-lookup"><span data-stu-id="76e48-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="76e48-201">Vyberte kartu **Transformace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-201">Select the **Transformations** tab.</span></span>

    ![Karta Transformace pro element BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="76e48-203">Jak vidíte, transformace **odstranit nealfanumerické** je nakonfigurována tak, aby používala výraz, který zkrátí mezery z poskytovaného textového řetězce.</span><span class="sxs-lookup"><span data-stu-id="76e48-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="76e48-204">Spusťte ladění v návrháři operací</span><span class="sxs-lookup"><span data-stu-id="76e48-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="76e48-205">Když konfigurujete pracovní verzi formátu ER, kterou lze spustit přímo z Návrháře operací, můžete získat přístup k ladicímu programu zdroje dat výběrem možnosti **Spustit ladění** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="76e48-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Tlačítko Spustit ladění na stránce Návrhář formátu](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="76e48-207">Mapování formátu a komponenty formátu ER, který je upravován, jsou k dispozici pro ladění.</span><span class="sxs-lookup"><span data-stu-id="76e48-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="76e48-208">Spusťte ladění v návrháři mapování modelu</span><span class="sxs-lookup"><span data-stu-id="76e48-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="76e48-209">Když konfigurujete mapování modelu ER, které lze spustit ze stránky **Mapování modelu** můžete získat přístup k lacicímu programu zdroje dat výběrem možnosti **Spustit ladění** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="76e48-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Tlačítko Spustit ladění na stránce vývojáře Mapování modelu](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="76e48-211">Komponenta mapování modelu mapování ER je k dispozici pro ladění.</span><span class="sxs-lookup"><span data-stu-id="76e48-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="76e48-212">Příloha 1: Získání řešení ER</span><span class="sxs-lookup"><span data-stu-id="76e48-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="76e48-213">Stažení řešení ER</span><span class="sxs-lookup"><span data-stu-id="76e48-213">Download an ER solution</span></span>

<span data-ttu-id="76e48-214">Pokud chcete použít řešení ER ke generování elektronického platebního souboru pro platbu zpracovanou prodejcem, můžete si [stáhnout](download-electronic-reporting-configuration-lcs.md) formát platby ER **Převod kreditu ISO20022**, který je k dispozici v knihovně Sdílený majetek ve službě Microsoft Dynamics Lifecycle Services (LCS) nebo v globálním úložišti.</span><span class="sxs-lookup"><span data-stu-id="76e48-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Import platebního formátu ER na stránce úložiště konfigurace](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="76e48-216">Kromě vybraného formátu ER musí být následující [konfigurace](general-electronic-reporting.md#Configuration) automaticky importovány do instance Microsoft Dynamics 365 Finance jako součást řešení ER **Převod úvěru ISO20022**:</span><span class="sxs-lookup"><span data-stu-id="76e48-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="76e48-217">**Model platby** [Konfigurace datového modelu ER](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="76e48-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="76e48-218">**Převod kreditu ISO20022** [Konfigurace formátu ER](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="76e48-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="76e48-219">**Mapování modelu platby 1611** [Konfigurace mapování modelu ER](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="76e48-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="76e48-220">**Mapování modelu platby do cíle ISO20022** Konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="76e48-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="76e48-221">Na stránce **Konfigurace** systému ER (**Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**) najdete následující konfigurace.</span><span class="sxs-lookup"><span data-stu-id="76e48-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Importované konfigurace na stránce konfigurace](./media/er-data-debugger-configurations.png)

<span data-ttu-id="76e48-223">Pokud v konfiguračním stromu chybí některá z dříve uvedených konfigurací, musíte je stáhnout ručně z knihovny sdílených položek LCS stejným způsobem, jakým jste stáhli formát platby ER **Převod kreditu ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="76e48-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="76e48-224">Analýza staženého řešení ER</span><span class="sxs-lookup"><span data-stu-id="76e48-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="76e48-225">Kontrola mapování modelu</span><span class="sxs-lookup"><span data-stu-id="76e48-225">Review the model mapping</span></span>

1. <span data-ttu-id="76e48-226">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="76e48-227">Vyberte **Platební model** \> **Mapování platebního modelu 1611**.</span><span class="sxs-lookup"><span data-stu-id="76e48-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="76e48-228">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="76e48-228">Select **Designer**.</span></span>
4. <span data-ttu-id="76e48-229">Vyberte záznam mapování **Mapování platebního modelu ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="76e48-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="76e48-230">Vyberte **Návrhář** a poté zkontrolujte otevřené mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="76e48-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="76e48-231">Všimněte si, že pole datového modelu **Platby** je vázáno na zdroj dat **\$notSentTransactions**, který vrací seznam zpracovávaných řádků platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="76e48-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Pole Platby na stránce Návrhář mapování modelů](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="76e48-233">Kontrola mapování formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-233">Review the format mapping</span></span>

1. <span data-ttu-id="76e48-234">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="76e48-235">Vyberte **Platební model** \> **Převod kreditu ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="76e48-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="76e48-236">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="76e48-236">Select **Designer**.</span></span>
4. <span data-ttu-id="76e48-237">Na kartě **Mapování** zkontrolujte otevřené mapování formátu.</span><span class="sxs-lookup"><span data-stu-id="76e48-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="76e48-238">Všimněte si, že je element **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** souboru **ISO20022CTReports** \> **XMLHeader** vázán na zdroj dat **\$PaymentByDebtor**, který je konfigurován na seskupení záznamů pole **Platby** datového modelu.</span><span class="sxs-lookup"><span data-stu-id="76e48-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![Element PmtInf na stránce Návrhář formátu](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="76e48-240">Kontrola formátu</span><span class="sxs-lookup"><span data-stu-id="76e48-240">Review the format</span></span>

1. <span data-ttu-id="76e48-241">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="76e48-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="76e48-242">Vyberte **Platební model** \> **Převod kreditu ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="76e48-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="76e48-243">Vyberte **Návrhář** a poté zkontrolujte otevřený formát.</span><span class="sxs-lookup"><span data-stu-id="76e48-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="76e48-244">Všimněte si, že element formátu v části **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** je konfigurován na zadání kódu IBAN účtu dodavatele v souboru platby.</span><span class="sxs-lookup"><span data-stu-id="76e48-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![Element BankIBAN na stránce Návrhář formátu](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="76e48-246">Příloha 2: Konfigurace pohledávek</span><span class="sxs-lookup"><span data-stu-id="76e48-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="76e48-247">Změna vlastnosti dodavatele</span><span class="sxs-lookup"><span data-stu-id="76e48-247">Modify a vendor property</span></span>

1. <span data-ttu-id="76e48-248">Přejděte do části **Pohledávky** \> **Dodavatelé** \> **Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="76e48-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="76e48-249">Vyberte dodavatele **DE-01002** a pak v podokně akcí na kartě **Dodavatel** ve skupině **Nastavení** vyberte **Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="76e48-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="76e48-250">Na pevné záložce **Identifikace** v okně **IBAN** <a name="enteredIBANcode"></a>zadejte **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="76e48-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="76e48-251">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="76e48-251">Select **Save**.</span></span>

![Pole IBAN nastavené na stránce Bankovní účty dodavatele](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="76e48-253">Nastavení způsobu platby</span><span class="sxs-lookup"><span data-stu-id="76e48-253">Set up a method of payment</span></span>

1. <span data-ttu-id="76e48-254">Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.</span><span class="sxs-lookup"><span data-stu-id="76e48-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="76e48-255">Vyberte způsob platby **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="76e48-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="76e48-256">Na pevné záložce **Formáty souboru** v části **Formáty souboru** nastavte možnost **Obecný formát elektronického exportu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="76e48-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="76e48-257">V poli **Exportovat konfiguraci formátu** vyberte formát **Převod kreditu ISO20022** ER.</span><span class="sxs-lookup"><span data-stu-id="76e48-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="76e48-258">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="76e48-258">Select **Save**.</span></span>

![Nastavení formátu souboru na stránce Způsoby platby](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="76e48-260">Přidání platby dodavatele</span><span class="sxs-lookup"><span data-stu-id="76e48-260">Add a vendor payment</span></span>

1. <span data-ttu-id="76e48-261">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="76e48-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="76e48-262">Přidejte nový deník plateb.</span><span class="sxs-lookup"><span data-stu-id="76e48-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="76e48-263">Vyberte **Řádky** a přidejte nový řádek platby.</span><span class="sxs-lookup"><span data-stu-id="76e48-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="76e48-264">V poli **Účet** vyberte dodavatele **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="76e48-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="76e48-265">Zadejte hodnotu do pole **Má dáti**.</span><span class="sxs-lookup"><span data-stu-id="76e48-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="76e48-266">V poli **Způsob platby** vyberte **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="76e48-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="76e48-267">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="76e48-267">Select **Save**.</span></span>

![Platba dodavatele přidaná na stránce Platby dodavatele](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="76e48-269">Příloha 3: Zpracování platby dodavatele</span><span class="sxs-lookup"><span data-stu-id="76e48-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="76e48-270">Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="76e48-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="76e48-271">Na stránce **Deník platby dodavatele** vyberte dříve vytvořený deník platby a pak vyberte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="76e48-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="76e48-272">Vyberte řádek platby a poté vyberte **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="76e48-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="76e48-273">Vyberte **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="76e48-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="76e48-274">V poli **Způsob platby** vyberte **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="76e48-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="76e48-275">V poli **Bankovní účet** vyberte **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="76e48-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="76e48-276">V dialogovém okně **Generovat platby** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76e48-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="76e48-277">V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76e48-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]