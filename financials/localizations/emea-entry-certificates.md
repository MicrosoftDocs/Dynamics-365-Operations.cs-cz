---
title: "Vstupní certifikáty EU"
description: "V tomto článku jsou informace o vstupních certifikátech Evropské unie (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11464
ms.assetid: e2240f55-cc9a-4ba4-ad50-2d919bca3b7f
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: a951b1f0159ef61704fb772d81ab6a9bc1c80589
ms.lasthandoff: 03/31/2017


---

# <a name="eu-entry-certificates"></a>Vstupní certifikáty EU

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o vstupních certifikátech Evropské unie (EU).

K dispozici máte následující úkoly pro vstupní certifikáty Evropské unie (EU):

-   Vytvoření a vystavení vstupního certifikátu EU spolu s dodacím listem nebo fakturou odběratele pro dodávku zboží nebo služby do zemí/regionů EU.
-   Zobrazení vstupního certifikátu EU s podpisem zákazníka EU.
-   Odeslání podepsaného vstupního certifikátu EU přijatého od odběratele nebo třetí strany odpovědné za dodání položek odběrateli.
-   Přidružení odeslaného vstupního certifikátu EU k faktuře odběratele.
-   Aktualizace stavu odeslaného vstupního certifikátu EU.

## <a name="prerequisites"></a>Požadavky
Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Předpoklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Země / oblast</td>
<td>Primární adresa právnické osoby musí být v členském státě EU.</td>
</tr>
<tr class="even">
<td>Související úkoly nastavení</td>
<td><ul>
<li>Na stránce <strong>Parametry pohledávek</strong> vyberte možnosti <strong>Povolit správu vstupních certifikátů</strong> a <strong>Povolit vystavování vstupních certifikátů</strong>.</li>
<li>Na stránce <strong>Odběratelé</strong> na pevné záložce <strong>Faktury a dodávky</strong> vyberte možnost <strong>Požadován vstupní certifikát</strong>, čímž označíte, že vstupní certifikát EU je povinný pro odběratele. Vyberte možnost <strong>Vystavit vstupní certifikát</strong>, pokud chcete vystavit vstupní certifikát EU právnické osoby pro odběratele.</li>
<li>Na stránce <strong>Parametry pohledávek</strong> vyberte kód číselné řady pro odkaz <strong>Vstupní certifikát</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Související transakce</td>
<td><ul>
<li>Vytvoření účtu odběratele.</li>
<li>Vytvořte prodejní objednávku.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>Vytváření, registrace a odesílání vstupního certifikátu EU
Vstupní certifikát EU můžete vytvořit automaticky nebo ručně. Vytvoří a vytiskne automaticky při zaúčtování dodacího listu nebo faktury pro zákazníka pomocí vstupní certifikát EU **dodací list účtování** stránky nebo **zaúčtování faktury** stránky. Chcete-li ručně vytvořit nebo znovu vytisknout vstupní certifikát EU pro fakturu odběratele, použijte **deník faktur** stránky. Dále můžete zadat podrobnosti o vstupním certifikátu EU vystaveném třetí stranou na stránce **Deník vstupního certifikátu**.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>Vytváření vstupního certifikátu EU automaticky nebo ručně

Vstupní certifikát EU můžete vytvořit automaticky pomocí dodacího listu na stránce **Všechny prodejní objednávky** nebo pomocí faktury na stránce **Prodejní objednávka**. Chcete-li ručně vytvořit vstupní certifikát EU, lze použít fakturu na stránce **Deník faktur**. Před ručním vytvořením vstupního certifikátu EU je však nutné změnit stav certifikátu faktury.

### <a name="registering-an-eu-entry-certificate"></a>Registrace vstupního certifikátu EU

Pokud je registrace povinná, můžete vstupní certifikát EU vystavený třetí stranou registrovat na stránce** Deník vstupního certifikátu**.

### <a name="uploading-a-received-eu-entry-certificate"></a>Odeslání přijatého vstupního certifikátu EU

Pomocí stránky **Přílohy** odešlete přijatý vstupní certifikát EU s podpisem zákazníka ze země EU. Poté, co je certifikát odeslán, je možné jej přiřadit k faktuře jako důkaz dodání položek. Tento doklad je vyžadován, pokud musíte vystavit fakturu, která neobsahuje daň z přidané hodnoty (DPH), a používá se rovněž při auditu.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Volitelné: Aktualizace stavu certifikátu a tisk stavu faktury

Můžete aktualizovat stav vstupního certifikátu a stav tisku faktury odběratele pomocí stránky **Deník faktur**.

## <a name="technical-information-for-system-administrators"></a>Technické informace pro správce systému
Pokud nemáte přístup ke stránkám, které se používají k dokončení tohoto úkolu, obraťte se na správce systému a poskytněte informace, které jsou uvedeny v následující tabulce.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Předpoklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Role a funkční oprávnění zabezpečení</td>
<td>K nastavení a vytvoření vstupních certifikátů EU pro produkty nebo služby musíte být členem role zabezpečení, která zahrnuje následující úkoly:
<ul>
<li><strong>Úředník pohledávek</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Zástupce odběratelského servisu</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Úředník prodeje</strong> (TradeSalesClerk)</li>
<li><strong>Úředník expedice</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>






