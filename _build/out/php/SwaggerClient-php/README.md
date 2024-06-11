# SwaggerClient-php
The REST API provided by BillaBear

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen
For more information, please visit [http://www.billabear.com/support](http://www.billabear.com/support)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/billabear/php-sdk.git"
    }
  ],
  "require": {
    "billabear/php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiKeyAuth
$config = BillaBear\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = BillaBear\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new BillaBear\Api\CheckoutApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \BillaBear\Model\CheckoutBody(); // \BillaBear\Model\CheckoutBody | 

try {
    $result = $apiInstance->createCheckout($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckoutApi->createCheckout: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://{customerId}.billabear.cloud/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CheckoutApi* | [**createCheckout**](docs/Api/CheckoutApi.md#createcheckout) | **POST** /checkout | Create Checkout
*CustomersApi* | [**addSeatsSubscriptions**](docs/Api/CustomersApi.md#addseatssubscriptions) | **POST** /subscription/{subscriptionId}/seats/add | Add Seats
*CustomersApi* | [**applyVoucherToCustomer**](docs/Api/CustomersApi.md#applyvouchertocustomer) | **POST** /customer/{customerId}/voucher | Apply voucher
*CustomersApi* | [**createCustomer**](docs/Api/CustomersApi.md#createcustomer) | **POST** /customer | Create
*CustomersApi* | [**disableCustomer**](docs/Api/CustomersApi.md#disablecustomer) | **POST** /customer/{customerId}/disable | Disable Customer
*CustomersApi* | [**enableCustomer**](docs/Api/CustomersApi.md#enablecustomer) | **POST** /customer/{customerId}/enable | Enable Customer
*CustomersApi* | [**fetchCustomerById**](docs/Api/CustomersApi.md#fetchcustomerbyid) | **GET** /customer/{customerId} | Detail
*CustomersApi* | [**getForCustomer**](docs/Api/CustomersApi.md#getforcustomer) | **GET** /customer/{customerId}/subscription | List Customer Subscriptions
*CustomersApi* | [**listCustomerInvoices**](docs/Api/CustomersApi.md#listcustomerinvoices) | **GET** /customer/{customerId}/invoices | List Customer Invoices
*CustomersApi* | [**listCustomerPayment**](docs/Api/CustomersApi.md#listcustomerpayment) | **GET** /customer/{customerId}/payment | List Customer Payments
*CustomersApi* | [**listCustomerRefund**](docs/Api/CustomersApi.md#listcustomerrefund) | **GET** /customer/{customerId}/refund | List Customer Refunds
*CustomersApi* | [**listCustomers**](docs/Api/CustomersApi.md#listcustomers) | **GET** /customer | List
*CustomersApi* | [**listPaymentDetails**](docs/Api/CustomersApi.md#listpaymentdetails) | **GET** /customer/{customerId}/payment-methods | List Customer&#x27;s Payment Details
*CustomersApi* | [**removeSeatsSubscriptions**](docs/Api/CustomersApi.md#removeseatssubscriptions) | **POST** /subscription/{subscriptionId}/seats/remove | Remove Seats
*CustomersApi* | [**showCustomerLimitsById**](docs/Api/CustomersApi.md#showcustomerlimitsbyid) | **GET** /customer/{customerId}/limits | Fetch Customer Limits
*CustomersApi* | [**updateCustomer**](docs/Api/CustomersApi.md#updatecustomer) | **PUT** /customer/{customerId} | Update
*InvoicesApi* | [**chargeInvoice**](docs/Api/InvoicesApi.md#chargeinvoice) | **POST** /invoice/{invoiceId}/charge | Charge Invoice
*InvoicesApi* | [**downloadInvoice**](docs/Api/InvoicesApi.md#downloadinvoice) | **GET** /invoice/{invoiceId}/download | Download Invoice
*InvoicesApi* | [**listCustomerInvoices**](docs/Api/InvoicesApi.md#listcustomerinvoices) | **GET** /customer/{customerId}/invoices | List Customer Invoices
*PaymentDetailsApi* | [**completeFrontendPaymentDetails**](docs/Api/PaymentDetailsApi.md#completefrontendpaymentdetails) | **POST** /customer/{customerId}/payment-methods/frontend-payment-token | Complete Frontend Detail Collection
*PaymentDetailsApi* | [**deletePaymentDetails**](docs/Api/PaymentDetailsApi.md#deletepaymentdetails) | **DELETE** /payment-methods/{paymentDetailsId} | Delete
*PaymentDetailsApi* | [**deletePaymentDetailsCustomer**](docs/Api/PaymentDetailsApi.md#deletepaymentdetailscustomer) | **DELETE** /customer/{customerId}/payment-methods/{paymentDetailsId} | Delete With Customer
*PaymentDetailsApi* | [**getPaymentDetails**](docs/Api/PaymentDetailsApi.md#getpaymentdetails) | **GET** /payment-methods/{paymentDetailsId} | Fetch
*PaymentDetailsApi* | [**listPaymentDetails**](docs/Api/PaymentDetailsApi.md#listpaymentdetails) | **GET** /customer/{customerId}/payment-methods | List Customer&#x27;s Payment Details
*PaymentDetailsApi* | [**makeDefaultPaymentDetails**](docs/Api/PaymentDetailsApi.md#makedefaultpaymentdetails) | **POST** /payment-methods/{paymentDetailsId}/default | Make Default
*PaymentDetailsApi* | [**makeDefaultPaymentDetailsCustomer**](docs/Api/PaymentDetailsApi.md#makedefaultpaymentdetailscustomer) | **POST** /customer/{customerId}/payment-methods/{paymentDetailsId}/default | Make Default With Customer
*PaymentDetailsApi* | [**startFrontendPaymentDetails**](docs/Api/PaymentDetailsApi.md#startfrontendpaymentdetails) | **GET** /customer/{customerId}/payment-methods/frontend-payment-token | Start Frontend Detail Collection
*PaymentsApi* | [**chargeInvoice**](docs/Api/PaymentsApi.md#chargeinvoice) | **POST** /invoice/{invoiceId}/charge | Charge Invoice
*PaymentsApi* | [**downloadInvoice**](docs/Api/PaymentsApi.md#downloadinvoice) | **GET** /invoice/{invoiceId}/download | Download Invoice
*PaymentsApi* | [**downloadReceipt**](docs/Api/PaymentsApi.md#downloadreceipt) | **GET** /receipt/{receiptId}/download | Download Receipt
*PaymentsApi* | [**listCustomerInvoices**](docs/Api/PaymentsApi.md#listcustomerinvoices) | **GET** /customer/{customerId}/invoices | List Customer Invoices
*PaymentsApi* | [**listCustomerPayment**](docs/Api/PaymentsApi.md#listcustomerpayment) | **GET** /customer/{customerId}/payment | List Customer Payments
*PaymentsApi* | [**listPayment**](docs/Api/PaymentsApi.md#listpayment) | **GET** /payment | List
*PaymentsApi* | [**refundPayment**](docs/Api/PaymentsApi.md#refundpayment) | **POST** /payment/{paymentId}/refund | Refund Payment
*PricesApi* | [**createPrice**](docs/Api/PricesApi.md#createprice) | **POST** /product/{productId}/price | Create
*PricesApi* | [**listPrice**](docs/Api/PricesApi.md#listprice) | **GET** /product/{productId}/price | List
*ProductsApi* | [**createProduct**](docs/Api/ProductsApi.md#createproduct) | **POST** /product | Create
*ProductsApi* | [**listProduct**](docs/Api/ProductsApi.md#listproduct) | **GET** /product | List
*ProductsApi* | [**showProductById**](docs/Api/ProductsApi.md#showproductbyid) | **GET** /product/{productId} | Detail
*ProductsApi* | [**updateProduct**](docs/Api/ProductsApi.md#updateproduct) | **PUT** /product/{productId} | Update
*ReceiptApi* | [**downloadReceipt**](docs/Api/ReceiptApi.md#downloadreceipt) | **GET** /receipt/{receiptId}/download | Download Receipt
*RefundsApi* | [**listCustomerRefund**](docs/Api/RefundsApi.md#listcustomerrefund) | **GET** /customer/{customerId}/refund | List Customer Refunds
*RefundsApi* | [**listRefund**](docs/Api/RefundsApi.md#listrefund) | **GET** /refund | List
*RefundsApi* | [**showRefundById**](docs/Api/RefundsApi.md#showrefundbyid) | **GET** /refund/{refundId} | Detail
*SubscriptionsApi* | [**addSeatsSubscriptions**](docs/Api/SubscriptionsApi.md#addseatssubscriptions) | **POST** /subscription/{subscriptionId}/seats/add | Add Seats
*SubscriptionsApi* | [**cancelSubscription**](docs/Api/SubscriptionsApi.md#cancelsubscription) | **POST** /subscription/{subscriptionId}/cancel | Cancel Subscription
*SubscriptionsApi* | [**changeSubscriptionPrice**](docs/Api/SubscriptionsApi.md#changesubscriptionprice) | **POST** /subscription/{subscriptionId}/price | Change Price
*SubscriptionsApi* | [**customerChangeSubscriptionPlan**](docs/Api/SubscriptionsApi.md#customerchangesubscriptionplan) | **POST** /subscription/{subscriptionId}/plan | Change Subscription Plan
*SubscriptionsApi* | [**customerStartSubscription**](docs/Api/SubscriptionsApi.md#customerstartsubscription) | **POST** /customer/{customerId}/subscription/start | Start Subscription For Customer
*SubscriptionsApi* | [**getForCustomer**](docs/Api/SubscriptionsApi.md#getforcustomer) | **GET** /customer/{customerId}/subscription | List Customer Subscriptions
*SubscriptionsApi* | [**listSubscriptionPlans**](docs/Api/SubscriptionsApi.md#listsubscriptionplans) | **GET** /subscription/plans | List Subscription Plans
*SubscriptionsApi* | [**listSubscriptions**](docs/Api/SubscriptionsApi.md#listsubscriptions) | **GET** /subscription | List
*SubscriptionsApi* | [**removeSeatsSubscriptions**](docs/Api/SubscriptionsApi.md#removeseatssubscriptions) | **POST** /subscription/{subscriptionId}/seats/remove | Remove Seats
*SubscriptionsApi* | [**showSubscriptionById**](docs/Api/SubscriptionsApi.md#showsubscriptionbyid) | **GET** /subscription/{subscriptionId} | Detail

## Documentation For Models

 - [Address](docs/Model/Address.md)
 - [CheckoutBody](docs/Model/CheckoutBody.md)
 - [CheckoutItems](docs/Model/CheckoutItems.md)
 - [CheckoutSubscriptions](docs/Model/CheckoutSubscriptions.md)
 - [Customer](docs/Model/Customer.md)
 - [CustomerIdVoucherBody](docs/Model/CustomerIdVoucherBody.md)
 - [Error](docs/Model/Error.md)
 - [Feature](docs/Model/Feature.md)
 - [FrontendToken](docs/Model/FrontendToken.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse20010](docs/Model/InlineResponse20010.md)
 - [InlineResponse20011](docs/Model/InlineResponse20011.md)
 - [InlineResponse20012](docs/Model/InlineResponse20012.md)
 - [InlineResponse20013](docs/Model/InlineResponse20013.md)
 - [InlineResponse2002](docs/Model/InlineResponse2002.md)
 - [InlineResponse2003](docs/Model/InlineResponse2003.md)
 - [InlineResponse2004](docs/Model/InlineResponse2004.md)
 - [InlineResponse2004Data](docs/Model/InlineResponse2004Data.md)
 - [InlineResponse2004Lines](docs/Model/InlineResponse2004Lines.md)
 - [InlineResponse2005](docs/Model/InlineResponse2005.md)
 - [InlineResponse2006](docs/Model/InlineResponse2006.md)
 - [InlineResponse2007](docs/Model/InlineResponse2007.md)
 - [InlineResponse2007Data](docs/Model/InlineResponse2007Data.md)
 - [InlineResponse2007Receipts](docs/Model/InlineResponse2007Receipts.md)
 - [InlineResponse2008](docs/Model/InlineResponse2008.md)
 - [InlineResponse2009](docs/Model/InlineResponse2009.md)
 - [InlineResponse201](docs/Model/InlineResponse201.md)
 - [InlineResponse201BillingAdmin](docs/Model/InlineResponse201BillingAdmin.md)
 - [InlineResponse201Lines](docs/Model/InlineResponse201Lines.md)
 - [InlineResponse400](docs/Model/InlineResponse400.md)
 - [Limit](docs/Model/Limit.md)
 - [PaymentDetails](docs/Model/PaymentDetails.md)
 - [PaymentIdRefundBody](docs/Model/PaymentIdRefundBody.md)
 - [Price](docs/Model/Price.md)
 - [Product](docs/Model/Product.md)
 - [ProductTaxType](docs/Model/ProductTaxType.md)
 - [SeatsAddBody](docs/Model/SeatsAddBody.md)
 - [SeatsRemoveBody](docs/Model/SeatsRemoveBody.md)
 - [Subscription](docs/Model/Subscription.md)
 - [SubscriptionIdCancelBody](docs/Model/SubscriptionIdCancelBody.md)
 - [SubscriptionIdPlanBody](docs/Model/SubscriptionIdPlanBody.md)
 - [SubscriptionIdPriceBody](docs/Model/SubscriptionIdPriceBody.md)
 - [SubscriptionPlan](docs/Model/SubscriptionPlan.md)
 - [SubscriptionStartBody](docs/Model/SubscriptionStartBody.md)

## Documentation For Authorization


## ApiKeyAuth

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Author

support@billabear.com
