# API Overview

## Purpose

This document gives a high-level view of the main API endpoints needed to support the order fulfillment and delivery tracking system.

The API supports order creation, delivery assignment, status updates, and order lookup.

## Endpoints

## Create Order

`POST /api/orders`

Creates a new customer order.

Example request:

```json
{
  "customer_name": "Dublin Office Supplies",
  "customer_phone": "+353871112222",
  "delivery_address": "Sandyford Business Park, Dublin",
  "requested_delivery_date": "2026-05-04",
  "order_reference": "DOS-1842",
  "delivery_notes": "Reception closes at 17:00"
}
```

Example response:

```json
{
  "order_id": "ORD-10045",
  "status": "Pending",
  "created_at": "2026-05-01T09:20:00"
}
```

## Fetch Orders

`GET /api/orders`

Returns a list of orders.

Optional query parameters:

- `status`
- `driver_id`
- `delivery_date`
- `delayed`

Example:

`GET /api/orders?status=Delayed`

## Fetch Single Order

`GET /api/orders/{order_id}`

Returns full order details, current delivery status, assigned driver, and status history.

## Assign Delivery

`POST /api/deliveries/assign`

Assigns an order to a driver.

Example request:

```json
{
  "order_id": "ORD-10045",
  "driver_id": "DRV-008",
  "planned_delivery_time": "2026-05-04T14:00:00"
}
```

Example response:

```json
{
  "delivery_id": "DEL-5021",
  "order_id": "ORD-10045",
  "driver_id": "DRV-008",
  "status": "Assigned"
}
```

## Update Status

`PATCH /api/orders/{order_id}/status`

Updates the status of an order or delivery.

Example request:

```json
{
  "status": "Out for Delivery",
  "note": "Driver left depot at 13:10"
}
```

Example response:

```json
{
  "order_id": "ORD-10045",
  "status": "Out for Delivery",
  "updated_at": "2026-05-04T13:12:00"
}
```

## Dashboard Summary

`GET /api/dashboard/summary`

Returns operational KPI counts.

Example response:

```json
{
  "orders_pending": 18,
  "deliveries_delayed": 4,
  "completed_today": 37,
  "average_delivery_time_minutes": 92
}
```

## API Notes

- All endpoints require authenticated access.
- Customer support users should not receive internal driver notes unless approved.
- Status updates should always create a history record.
- The first release does not include public customer tracking endpoints.

