.. code-block:: bash 
    
    # get meta data for OrderResource
    curl -H "Content-Type: application/json" \
         -H "Authorization: User:1" \
         http://localhost:5000/meta/orders/single
    
    
..

.. code-block:: json 

    {
        "model_class": "Order",
        "url_prefix": "/",
        "url": "/orders",
        "methods": {
            "get": {
                "url": "/orders",
                "requirements": [
                    "mock_jwt_required"
                ],
                "input": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    }
                },
                "responses": {
                    "fields": {
                        "owner_id": {
                            "type": "integer",
                            "format": "int32",
                            "nullable": false,
                            "foreign_key": "user.id",
                            "info": {}
                        },
                        "id": {
                            "type": "integer",
                            "format": "int32",
                            "primary_key": true,
                            "nullable": true,
                            "info": {}
                        },
                        "ordered_at": {
                            "type": "date-time",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": "datetime.now",
                                "is_clause_element": false,
                                "is_callable": true,
                                "is_scalar": false
                            },
                            "info": {}
                        },
                        "description": {
                            "type": "string",
                            "nullable": false,
                            "info": {}
                        },
                        "status_id": {
                            "type": "integer",
                            "format": "int8",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": 0,
                                "is_clause_element": false,
                                "is_callable": false,
                                "is_scalar": true
                            },
                            "info": {}
                        }
                    }
                }
            },
            "post": {
                "requirements": [
                    "mock_jwt_required"
                ],
                "input": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    },
                    "ownerId": {
                        "type": "integer",
                        "format": "int32",
                        "nullable": false,
                        "foreign_key": "user.id",
                        "info": {}
                    },
                    "description": {
                        "type": "string",
                        "nullable": false,
                        "info": {}
                    },
                    "orderedAt": {
                        "type": "date-time",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": "datetime.now",
                            "is_clause_element": false,
                            "is_callable": true,
                            "is_scalar": false
                        },
                        "info": {}
                    },
                    "statusId": {
                        "type": "integer",
                        "format": "int8",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": 0,
                            "is_clause_element": false,
                            "is_callable": false,
                            "is_scalar": true
                        },
                        "info": {}
                    }
                },
                "responses": {
                    "fields": {
                        "owner_id": {
                            "type": "integer",
                            "format": "int32",
                            "nullable": false,
                            "foreign_key": "user.id",
                            "info": {}
                        },
                        "id": {
                            "type": "integer",
                            "format": "int32",
                            "primary_key": true,
                            "nullable": true,
                            "info": {}
                        },
                        "ordered_at": {
                            "type": "date-time",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": "datetime.now",
                                "is_clause_element": false,
                                "is_callable": true,
                                "is_scalar": false
                            },
                            "info": {}
                        },
                        "description": {
                            "type": "string",
                            "nullable": false,
                            "info": {}
                        },
                        "status_id": {
                            "type": "integer",
                            "format": "int8",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": 0,
                                "is_clause_element": false,
                                "is_callable": false,
                                "is_scalar": true
                            },
                            "info": {}
                        }
                    }
                }
            },
            "put": {
                "url": "/orders",
                "requirements": [
                    "mock_jwt_required"
                ],
                "input": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    },
                    "ownerId": {
                        "type": "integer",
                        "format": "int32",
                        "nullable": false,
                        "foreign_key": "user.id",
                        "info": {}
                    },
                    "description": {
                        "type": "string",
                        "nullable": false,
                        "info": {}
                    },
                    "orderedAt": {
                        "type": "date-time",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": "datetime.now",
                            "is_clause_element": false,
                            "is_callable": true,
                            "is_scalar": false
                        },
                        "info": {}
                    },
                    "statusId": {
                        "type": "integer",
                        "format": "int8",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": 0,
                            "is_clause_element": false,
                            "is_callable": false,
                            "is_scalar": true
                        },
                        "info": {}
                    }
                },
                "responses": {
                    "fields": {
                        "owner_id": {
                            "type": "integer",
                            "format": "int32",
                            "nullable": false,
                            "foreign_key": "user.id",
                            "info": {}
                        },
                        "id": {
                            "type": "integer",
                            "format": "int32",
                            "primary_key": true,
                            "nullable": true,
                            "info": {}
                        },
                        "ordered_at": {
                            "type": "date-time",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": "datetime.now",
                                "is_clause_element": false,
                                "is_callable": true,
                                "is_scalar": false
                            },
                            "info": {}
                        },
                        "description": {
                            "type": "string",
                            "nullable": false,
                            "info": {}
                        },
                        "status_id": {
                            "type": "integer",
                            "format": "int8",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": 0,
                                "is_clause_element": false,
                                "is_callable": false,
                                "is_scalar": true
                            },
                            "info": {}
                        }
                    }
                }
            },
            "patch": {
                "url": "/orders",
                "requirements": [
                    "mock_jwt_required"
                ],
                "input": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    },
                    "ownerId": {
                        "type": "integer",
                        "format": "int32",
                        "nullable": false,
                        "foreign_key": "user.id",
                        "info": {}
                    },
                    "description": {
                        "type": "string",
                        "nullable": false,
                        "info": {}
                    },
                    "orderedAt": {
                        "type": "date-time",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": "datetime.now",
                            "is_clause_element": false,
                            "is_callable": true,
                            "is_scalar": false
                        },
                        "info": {}
                    },
                    "statusId": {
                        "type": "integer",
                        "format": "int8",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": 0,
                            "is_clause_element": false,
                            "is_callable": false,
                            "is_scalar": true
                        },
                        "info": {}
                    }
                },
                "responses": {
                    "fields": {
                        "owner_id": {
                            "type": "integer",
                            "format": "int32",
                            "nullable": false,
                            "foreign_key": "user.id",
                            "info": {}
                        },
                        "id": {
                            "type": "integer",
                            "format": "int32",
                            "primary_key": true,
                            "nullable": true,
                            "info": {}
                        },
                        "ordered_at": {
                            "type": "date-time",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": "datetime.now",
                                "is_clause_element": false,
                                "is_callable": true,
                                "is_scalar": false
                            },
                            "info": {}
                        },
                        "description": {
                            "type": "string",
                            "nullable": false,
                            "info": {}
                        },
                        "status_id": {
                            "type": "integer",
                            "format": "int8",
                            "nullable": true,
                            "default": {
                                "for_update": false,
                                "arg": 0,
                                "is_clause_element": false,
                                "is_callable": false,
                                "is_scalar": true
                            },
                            "info": {}
                        }
                    }
                }
            },
            "delete": {
                "url": "/orders",
                "requirements": [
                    "mock_jwt_required"
                ],
                "input": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    }
                },
                "responses": {}
            }
        },
        "table": {
            "Order": {
                "type": "object",
                "properties": {
                    "id": {
                        "type": "integer",
                        "format": "int32",
                        "primary_key": true,
                        "nullable": true,
                        "info": {}
                    },
                    "owner_id": {
                        "type": "integer",
                        "format": "int32",
                        "nullable": false,
                        "foreign_key": "user.id",
                        "info": {}
                    },
                    "description": {
                        "type": "string",
                        "nullable": false,
                        "info": {}
                    },
                    "ordered_at": {
                        "type": "date-time",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": "datetime.now",
                            "is_clause_element": false,
                            "is_callable": true,
                            "is_scalar": false
                        },
                        "info": {}
                    },
                    "status_id": {
                        "type": "integer",
                        "format": "int8",
                        "nullable": true,
                        "default": {
                            "for_update": false,
                            "arg": 0,
                            "is_clause_element": false,
                            "is_callable": false,
                            "is_scalar": true
                        },
                        "info": {}
                    }
                },
                "xml": "Order"
            }
        }
    }

..